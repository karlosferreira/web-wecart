<template>
    <div>
        <v-toolbar app flat>
            <div class="container toolbar-content">
                <LogoHeader/>
                <ShippingBox/>
                <CartBox/>
            </div>
        </v-toolbar>
        <!-- <ListCategories/> -->
    </div>
</template>

<script>
import LogoHeader from '@/components/LogoHeader';
import ShippingBox from '@/components/ShippingBox';
import CartBox from '@/components/CartBox';
import ListCategories from '@/components/ListCategories';

export default {
  name: 'Header',
  components: {
    LogoHeader,
    ShippingBox,
    CartBox,
    ListCategories
  },
  // data () {
  //   return {}
  // }
}
</script>

<style>
  .application .theme--light.toolbar, .theme--light .toolbar {
    background-color: #17a2b8;
    color: rgb(255 255 255);
    min-height: 80px;
    box-shadow: none;
  }
  .toolbar-content{
    padding: 18px;
  }
</style>