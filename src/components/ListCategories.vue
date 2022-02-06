<template>
    <v-content class="categories-box">
      <v-card>
        <v-container>
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
              <!-- <v-btn class="ma-2" color="primary" dark>Pastas</v-btn>
              <v-btn class="ma-2" color="primary" dark>Cafés</v-btn>
              <v-btn class="ma-2" color="primary" dark>Complementos</v-btn>
              <v-btn class="ma-2" color="primary" dark>Suplementos</v-btn>
              <v-btn class="ma-2" color="primary" dark>Laticínios</v-btn>
              <v-btn class="ma-2" color="primary" dark>Padaria</v-btn> -->
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
        </v-container>
      </v-card>
    </v-content>  
</template>

<script>
export default {

}
</script>

<style>
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