<template>
    <v-content class="categories-box">    
      <v-card>
        <v-container>
          <div class="text-center">
            <div class="row">
              <v-btn 
                v-bind:key="category.id" 
                v-for="category in categories" 
                class="ma-2" 
                color="primary" 
                dark
              >
                <v-icon>{{category.cat_icon}}</v-icon>
                <span>{{category.cat_name}}</span>
              </v-btn>
            </div> 
          </div>
        </v-container>
      </v-card>
    </v-content>  
</template>

<script>
import categories from '@/data/categories.json';

export default {
  name: 'ListCategories',
  data () {
    return { categories }
  }
}
</script>

<style>
  .btn__content {
    background: #17a2b8;
  }
  button.ma-2.btn.theme--dark.primary {
    margin-left: auto;
    margin-right: auto;
    min-width: 176px;
    font-size: 13.5px;
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
  .btn .btn__content .icon {
    color: inherit;
    margin-right: 0.7vw;
  }  
</style>