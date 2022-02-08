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
    font-size: 36px;
    font-weight: 600;
    margin-left: 2.2vw;
    margin-right: 3.2vw;
    transform: translateY(-4px);
    cursor: pointer;    
    float: left;
  }
</style>