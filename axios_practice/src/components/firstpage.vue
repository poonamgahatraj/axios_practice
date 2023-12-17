<template>
<h1>hello</h1>
</template>

<script scoped>
import Vue from "vue";
import axios from "axios";
import VueAxios from "vue-axios";
Vue.use(axios, VueAxios);

export default {
  mounted() {
    Vue.axios
      .get("https://api.coindesk.com/v1/bpi/currentprice.json")
      .then((response) => {
        console.log(response);
      });
  },
};
</script>