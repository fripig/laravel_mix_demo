<template>
    <div>
        <div class="chart" ref="chart"></div>
    </div>
</template>

<script>
    import {bb} from 'billboard.js'
    export default {
        name: "Chart",
        data(){
          return {
              chart:null
          }
        },
        mounted() {
            this.chart = bb.generate({
                bindto: this.$refs.chart,
                data: {
                    type: "bar",
                    columns: [
                        ["data1", 30, 200, 100, 170, 150, 250],
                        ["data2", 130, 100, 140, 35, 110, 50]
                    ]
                }
            });
        }
    }
</script>

<style scoped>

</style>
