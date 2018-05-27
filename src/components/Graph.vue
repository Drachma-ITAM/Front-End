<template>
  <div class="graph-page">
    <nav-bar/>
    <canvas id="chartContainer"></canvas>
    <div class="estimado"></div>
  </div>
</template>

<script>
import NavBar from './global/NavBar'

export default {
  name: 'GraphPage',
  components: {
    'nav-bar': NavBar,
  },
  data () {
    return {
      wsocket: null,
      chart: null,
      xVal: 0,
      dataLenght: 1000,
      xLabel: [],
      dps: [],
      dpsc: ['rgba(0,0,0, 0.1)']
    }
  },
  methods: {
    onMessage: function (e) {
      var vm = this;
      var data = e.data;
      console.log( /accion":"(.*)?",/.exec(data)[0].replace('accion":"','').replace('",', '') );
      var price = /price : \d+.\d+/.exec(data)[0].replace('price : ','');
      vm.dps.push({x: new Date(), y: price});
      vm.xLabel.push(`${new Date()}`)
      vm.xVal++;
      if(vm.dps.length > 1) {
        var lastPrice = vm.dps[vm.dps.length - 2].y;
        if(lastPrice > Number(price)) {
          vm.dpsc.push('#ff0000');
          vm.$el.querySelector('.estimado').style.backgroundColor = 'red';
        }else if(lastPrice == Number(price)) {
          vm.dpsc.push('rgba(0,0,0, 0.1)');
          vm.$el.querySelector('.estimado').style.backgroundColor = 'black';
        }else {
          vm.dpsc.push('#00ff00');
          vm.$el.querySelector('.estimado').style.backgroundColor = 'green';
        }
      }
      vm.chart.update();
      vm.wsocket.send(JSON.stringify({
        type: 'update'
      }))
    }
  },
  mounted () {
    var vm = this;
    var ctx = vm.$el.querySelector('#chartContainer').getContext('2d');;
    this.chart = new Chart(ctx, {
      type: 'line',
      data: {
        labels: vm.xLabel,
        datasets: [{
          label: "USD$",
          data: vm.dps,
          pointBackgroundColor: vm.dpsc,
          fill: false,
          lineTension: 0,
        }]
      },
      options:  {
        title: {
          display: true,
          text: 'BTCUSD'
        }
      }
    })
    vm.wsocket = new WebSocket('ws://localhost:4040/ws/data');
    vm.wsocket.onmessage = vm.onMessage;
    vm.wsocket.onopen = function() {
      vm.wsocket.send(JSON.stringify({
        type: 'update'
      }))
    }
  }
}
</script>

<style scoped>
.graph-page {
  width: 100%;
  position: relative;
}

#chartContainer {
  height: 90vh;
  width: 95%;
}

.estimado {
  height: 80px;
  width: 80px;
  position: absolute;
  bottom: 0;
  right: 50px;
  background-color: red;
}
</style>
