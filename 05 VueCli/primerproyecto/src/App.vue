<template>
  <div id="app">
    <h1 class="title">Leonis Ocampo Nieves</h1>
    <h2 class="subtitle">Single File Component</h2>

    <HelloWorld msg="Welcome to Your Vue.js App" />

    <h3 class="title is-size-4">01. Primer componente</h3>
    <div class="box">
      <Timer></Timer>
    </div>

    <h3 class="title is-size-4">02. Segundo compoenente</h3>
    <h4 class="subtitle is-size-5">Con inicialización de propiedades</h4>
    <div class="box">
      <div>
        <Icon type="fa-user" message="Hola mundo"></Icon>
      </div>
      <div>
        <Icon type="fa-user"></Icon>
      </div>
    </div>

    <!--<h3 class="title is-size-4">03. Tercer compoenente</h3>
    <h4 class="subtitle is-size-5">Ejemplo mas avanzado</h4>
    <div class="box">
      <Currency culture="es-US" :amount="amount" />
      <Currency culture="es-US" :amount="amount" />
      <Currency culture="es-US" :amount="amount" />
    </div>-->

    <h3 class="title is-size-4">04. Shopping cart</h3>
    <h4 class="subtitle is-size-5">Components hijos y padres</h4>
    <div class="box">
      <ShoppingCart></ShoppingCart>
    </div>

    <h3 class="title is-size-4">05. Page View component</h3>
    <h4 class="subtitle is-size-5">Uso de slots</h4>
    <div class="box">
      <Page title="Soy una página con slot">
        <p>Hola, soy una página</p>
        <p>Hola mundo</p>
        <p>Leonis Ocampo Nieves</p>
        <p>Monto: {{amount}}</p>
      </Page>
    </div>
  </div>
</template>

<script>
import HelloWorld from "./components/HelloWorld.vue";
import Timer from "./components/Timer";
import Icon from "./components/Icon";
//import Currency from "./components/Currency";
import ShoppingCart from "./components/ShopingCart";
import Page from "./components/Page";

export default {
  name: "App",

  data() {
    return {
      amount: 100,
    };
  },

  components: {
    HelloWorld,
    Timer,
    Icon,
    //Currency,
    ShoppingCart,
    Page
  },
};
</script>

<style>
</style>