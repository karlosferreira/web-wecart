<template>
  <v-app>
    <Header/>
    <v-content class="loading-box">
      <div class="full-loading">
        <v-progress-circular indeterminate color="primary" class="dash-loading"></v-progress-circular>
      </div>
      <router-view/>
    </v-content>
    <ProductInfo/>
  </v-app>
</template>

<script>
import ProductInfo from '@/components/ProductInfo';
import Header from '@/components/Header';

export default {
  name: 'App',
  components: {
    Header,
    ProductInfo
  }
}
</script>

<style lang="css" scoped>
  .full-loading {
    display: table;
    width: 35px;
    height: 100%;
    margin-left: auto;
    margin-right: auto;
  }
  .dash-loading {
    margin-left: auto;
    margin-right: auto;
    vertical-align: middle;
    display: table-cell;
  }
</style>
