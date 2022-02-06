<template>
  <v-toolbar-title v-text="title"></v-toolbar-title>
</template>

<script>
export default {
  name: 'LogoHeader',
  // components: {},
  data () {
    return {
      title: 'WeCart'
    }
  } 
}
</script>

<style>
  .toolbar__title {
    font-size: 30px;
    font-weight: 600;
    margin-left: 0;
    float: left;
  }
</style>