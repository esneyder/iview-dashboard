<style media="screen">
  div > h1 {
    margin-bottom: 20px;
  }
</style>
<template>
    <div>
      <h1>Utilice iView para cargar archivos propios, cómodos y rápidos</h1>
      <Upload
          multiple
          type="drag"
          action="//jsonplaceholder.typicode.com/posts/">
          <div style="padding: 20px 0">
              <Icon type="ios-cloud-upload" size="52" style="color: #3399ff"></Icon>
              <p>Haga clic o arrastre el archivo aquí para cargarlo</p>
          </div>
      </Upload>
    </div>
</template>
<script>
    export default {

    }
</script>
