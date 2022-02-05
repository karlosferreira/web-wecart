<template>
  <v-app>
    <v-toolbar
    app
    flat>
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
          <!-- <v-icon>edit</v-icon> -->
        </div>        
        <!-- <v-icon>login</v-icon> -->
        <div class="cart-box">
          <v-icon>shopping_cart</v-icon>          
        </div>
      </div>
    </v-toolbar>
    <v-content class="categories-box">
      <v-card>
        <!-- <v-container>
          <div class="text-center">
            <div class="row">
              <v-btn class="ma-2" color="primary" dark>Bebidas</v-btn>
              <v-btn class="ma-2" color="primary" dark>Grãos</v-btn>
              <v-btn class="ma-2" color="primary" dark>Ferináceos</v-btn>
              <v-btn class="ma-2" color="primary" dark>Cereais</v-btn>
              <v-btn class="ma-2" color="primary" dark>Massas</v-btn>
              <v-btn class="ma-2" color="primary" dark>Molhos</v-btn>
              <v-btn class="ma-2" color="primary" dark>Conservas</v-btn>
              <v-btn class="ma-2" color="primary" dark>Enlatados</v-btn>
              <v-btn class="ma-2" color="primary" dark>Temperos</v-btn>
              <v-btn class="ma-2" color="primary" dark>Condimentos</v-btn>
              <v-btn class="ma-2" color="primary" dark>Aperitivos</v-btn>
              <v-btn class="ma-2" color="primary" dark>Biscoitos</v-btn>
              <v-btn class="ma-2" color="primary" dark>Doces</v-btn>
              <v-btn class="ma-2" color="primary" dark>Sobremesas</v-btn>
              <v-btn class="ma-2" color="primary" dark>Sopas</v-btn>
              <v-btn class="ma-2" color="primary" dark>Cremes</v-btn>
              <v-btn class="ma-2" color="primary" dark>Pastas</v-btn>
              <v-btn class="ma-2" color="primary" dark>Cafés</v-btn>
              <v-btn class="ma-2" color="primary" dark>Complementos</v-btn>
              <v-btn class="ma-2" color="primary" dark>Suplementos</v-btn>
              <v-btn class="ma-2" color="primary" dark>Laticínios</v-btn>
              <v-btn class="ma-2" color="primary" dark>Padaria</v-btn>
              <v-btn class="ma-2" color="primary" dark>Açougue</v-btn>
              <v-btn class="ma-2" color="primary" dark>Aviário</v-btn>
              <v-btn class="ma-2" color="primary" dark>Peixaria</v-btn>
              <v-btn class="ma-2" color="primary" dark>Congelados</v-btn>
              <v-btn class="ma-2" color="primary" dark>Defumados</v-btn>
              <v-btn class="ma-2" color="primary" dark>Chocolates</v-btn>
              <v-btn class="ma-2" color="primary" dark>Integrais</v-btn>
              <v-btn class="ma-2" color="primary" dark>Papinhas</v-btn>                                              
            </div> 
          </div>
        </v-container> -->
      </v-card>
    </v-content>
    <v-content class="loading-box">
      <div class="full-loading">
        <v-progress-circular indeterminate color="primary" class="dash-loading"></v-progress-circular>
      </div>
      <router-view/>
    </v-content>
    <!-- <v-footer :fixed="fixed" app>
      <span>&copy; 2017</span>
    </v-footer> -->
  </v-app>
</template>

<script>
export default {
  data () {
    return {
      clipped: false,
      drawer: true,
      fixed: false,
      items: [{
        icon: 'bubble_chart',
        title: 'Inspire'
      }],
      miniVariant: false,
      right: true,
      rightDrawer: false,
      title: 'WeCart'
    }
  },
  name: 'App'
}
</script>

<style lang="css" scoped>
  .center-toolbar {
    width: 100%!important;
  }
  .full-loading {
    display: table;
    width: 35px;
    height: 100%;
    margin-left: auto;
    margin-right: auto;
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
  .dash-loading {
    margin-left: auto;
    margin-right: auto;
    vertical-align: middle;
    display: table-cell;
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
  .input-read{
    color: #fff!important;
  }
  .input-read .input-group__input input[type="text"] {
    color: #fff!important;
  }
  .cart-box {
    position: absolute;
    right: 8vw;
    transform: translateY(-60px);
  }

  /* categories css */
  .btn__content {
    background: #17a2b8;
  }
  button.ma-2.btn.theme--dark.primary {
    min-width: 125px;
    margin-left: auto;
    margin-right: auto;
    font-size: 11px;
  }
  .categories-box {
    padding: 80px 0px 0px!important;
  }
  .categories-box .card {
    box-shadow: none;
  }  
  .categories-box .ma-2 {
    background:#343a40!important
  }
  .categories-box .ma-2:hover {
    background: #17a2b8!important;
  }
  .loading-box {
    padding: 0!important;
  }  
  /* end categories css */
</style>
