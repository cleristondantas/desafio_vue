<template>
    <div id="app">
        <div class="container header">
            <div class="row topo">
                <div class="col-lg-4 logo">
                    <img src="./assets/images/logo-8anos.svg">
                </div>
                <div class="col-lg-8"></div>
            </div>
        </div>
        <div class="container topo-principal">
            <div class="row">
                <div class="col-lg-6 botoes">
                    <button class="btn btn-primary">Fretes</button>
                    <button class="btn btn-danger">Empresas</button>
                    <button class="btn btn-success">Veiculos</button>
                </div>
                <div class="col-lg-6 login">

                </div>
            </div>
        </div>

        <div class="container conteudo">
            <div class="row">
            <tplfrete></tplfrete>
            </div>
        </div>

    </div>
</template>


<script>
import Tplfrete from './components/fretes.vue'

export default {
  name: 'app',
  components: {
      Tplfrete,
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
}

.obs-texto{
    height: 22px;
    background: #F9F9F9;
    padding: 3px 0 3px 5px;
}

.header {
    height: 119px;
}

.topo{
    padding-top: 23px;
}

.topo-principal {
    height: 105px;
}

.filtros{
    background: #E9E9E9;
    -webkit-border-radius: 10px;
    -moz-border-radius: 10px;
    -ms-border-radius: 10px;
    border-radius: 10px;
}

.frete{
    height: 100px;
    padding: 10px 0;
    font-size: 12px;
    color: #383838;
}

.dados-frete{
    height: 50px;
    overflow: hidden;
}

.logo-emp{
    height: 50px;
}

span {
    height: 25px;
    padding: 5px 0 5px 5px;
    overflow: hidden;
    float: left;
    width: 100%;
}
</style>


