<template>
  <Table border :columns="columns7" :data="data6"></Table>
</template>
<script>
  export default {
    data () {
      return {
        columns7: [
          {
            title: 'Nombre',
            key: 'name',
            render: (h, params) => {
              return h('div', [
                h('Icon', {
                  props: {
                    type: 'person'
                  }
                }),
                h('strong', params.row.name)
              ]);
            }
          },
          {
            title: 'Edad',
            key: 'age'
          },
          {
            title: 'Direccion',
            key: 'address'
          },
          {
            title: 'Operación',
            key: 'action',
            width: 150,
            align: 'center',
            render: (h, params) => {
              return h('div', [
                h('Button', {
                  props: {
                    type: 'primary',
                    size: 'small'
                  },
                  style: {
                    marginRight: '5px'
                  },
                  on: {
                    click: () => {
                      this.show(params.index)
                    }
                  }
                }, 'Detalle'),
                h('Button', {
                  props: {
                    type: 'error',
                    size: 'small'
                  },
                  on: {
                    click: () => {
                      this.remove(params.index)
                    }
                  }
                }, 'Borrar')
              ]);
            }
          }
        ],
        data6: [
          {
            name: 'Daniel Lopez',
            age: 18,
            address: 'Caracas'
          },
          {
            name: 'Maria Marcano',
            age: 25,
            address: 'Maturin'
          },
          {
            name: 'Jose Perez',
            age: 30,
            address: 'Carupano'
          },
          {
            name: 'Otoniela',
            age: 26,
            address: 'Valencia'
          },{
            name: 'Gregorys Arcia',
            age: 18,
            address: 'Merida'
          },
          {
            name: 'Jhon Garcia',
            age: 25,
            address: 'Upata'
          }
        ]
      }
    },
    methods: {
      show (index) {
        this.$Modal.info({
          title: 'Información del usuario',
          content: `Nombre：${this.data6[index].name}<br>Edad：${this.data6[index].age}<br>Dirección：${this.data6[index].address}`
        })
      },
      remove (index) {
        this.data6.splice(index, 1);
      }
    }
  }
</script>
