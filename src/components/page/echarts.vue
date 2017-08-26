<style scoped>
.echarts {
  margin-left: 20px;
}
.echarts-item {
    float: left;
    width: 500px;
    height: 400px;
}
</style>
<template>
<div class="echarts">
    <div class="echarts-item">
        <IEcharts :option="pie"></IEcharts>
    </div>
    <div class="echarts-item">
        <IEcharts :option="pie_radius"></IEcharts>
    </div>
    <div class="echarts-item">
        <IEcharts :option="line"></IEcharts>
    </div>
    <div class="echarts-item">
        <IEcharts :option="bar"></IEcharts>
    </div>
</div>
</template>
<script>
import IEcharts from 'vue-echarts-v3';
export default {
    components: {
        IEcharts
    },
    data: () => ({
        line: {
            title: {
                text: 'Curva'
            },
            xAxis: {
                data: ["Camisa", "sudadera", "camisa de gasa", "pantalones", "tacones altos", "calcetines"]
            },
            yAxis: {},
            series: [{
                name: "Ventas",
                type: "line",
                data: [5, 20, 36, 10, 10, 20]
            }]
        },
        bar: {
            title: {
                text: 'Histograma'
            },
            xAxis: {
                data: ["Camisa", "sudadera", "camisa de gasa", "pantalones", "tacones altos", "calcetines"]
            },
            yAxis: {},
            series: [{
                name: "销量",
                type: "bar",
                data: [5, 20, 36, 10, 10, 20]
            }]
        },
        pie: {

            title: {
                text: 'Gráfico circular',
                x: 'center'
            },
            tooltip: {
                trigger: 'item',
                formatter: "{a} <br/>{b} : {c} ({d}%)"
            },
            legend: {
                orient: 'vertical',
                left: 'left',
                data: ["Camisa", "suéter", "camisa de gasa", "pantalones", "tacones altos"]
            },
            series: [{
                name: 'Ventas',
                type: 'pie',
                radius: '55%',
                center: ['50%', '50%'],
                data: [{
                    value: 335,
                    name: 'Camisa'
                }, {
                    value: 310,
                    name: 'Suéter'
                }, {
                    value: 234,
                    name: 'Camisa de gasa'
                }, {
                    value: 135,
                    name: 'Pantalones'
                }, {
                    value: 548,
                    name: 'Tacones altos'
                }],
                itemStyle: {
                    emphasis: {
                        shadowBlur: 10,
                        shadowOffsetX: 0,
                        shadowColor: 'rgba(0, 0, 0, 0.5)'
                    }
                }
            }]
        },
        pie_radius: {

            title: {
                text: 'Diagrama de anillo',
                x: 'center'
            },
            tooltip: {
                trigger: 'item',
                formatter: "{a} <br/>{b} : {c} ({d}%)"
            },
            legend: {
                orient: 'vertical',
                left: 'left',
                data: ["Camisa", "suéter", "camisa de gasa", "pantalones", "tacones altos"]
            },
            series: [{
                name: 'Ventas',
                type: 'pie',
                radius: ['40%', '60%'],
                data: [{
                    value: 335,
                    name: 'Camisa'
                }, {
                    value: 310,
                    name: 'Suéter'
                }, {
                    value: 234,
                    name: 'Camisa de gasa'
                }, {
                    value: 135,
                    name: 'Pantalones'
                }, {
                    value: 548,
                    name: 'Tacones altos'
                }],
                itemStyle: {
                    emphasis: {
                        shadowBlur: 10,
                        shadowOffsetX: 0,
                        shadowColor: 'rgba(0, 0, 0, 0.5)'
                    }
                }
            }]
        }
    })
}
</script>
