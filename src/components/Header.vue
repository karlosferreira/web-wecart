<template>
    <div>
        <v-toolbar app flat>
            <div class="container toolbar-content">
                <v-toolbar-title v-text="title"></v-toolbar-title>
                <div class="shipping-box">
                <v-text-field
                    value="Rua Soldado Jacinto Costa, 22"
                    label="Endereço para entregas"
                    outlined
                    readonly
                    class="input-read"
                ></v-text-field>
                </div>        
                <div class="cart-box">
                    <v-icon>shopping_cart</v-icon>          
                </div>
            </div>
        </v-toolbar>
        <ListCategories/>
    </div>
</template>

<script>
import ListCategories from '@/components/ListCategories';

export default {
  name: 'Header',
  components: {
    ListCategories
  },
  data () {
    return {
      title: 'WeCart'
    }
  }  
}
</script>

<style>
  .center-toolbar {
    width: 100%!important;
  }
  .shipping-box {
    display: flex;
    width: 260px;
    margin-left: 20vw;
    margin-right: auto;
    transform: translateY(-5px);
  }
  .shipping-box i {
    transform: translate(-10px, -7px);
  }
  .application .theme--light.toolbar, .theme--light .toolbar {
    background-color: #17a2b8;
    color: rgb(255 255 255);
    min-height: 80px;
    box-shadow: none;
  }
  .toolbar__title {
    font-size: 30px;
    font-weight: 600;
    margin-left: 0;
    float: left;
  }
  .toolbar-content{
    padding: 18px;
  }
  .cart-box {
    position: absolute;
    right: 8vw;
    transform: translateY(-60px);
  }
  .shipping-box i {
    transform: translate(-10px, -7px);
  }  
  .input-read{
    color: #fff!important;
  }
  .input-read .input-group__input input[type="text"] {
    color: #fff!important;
  }  
</style>