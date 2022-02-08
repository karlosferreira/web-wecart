<template>
    <v-flex xs12 class="card-box" >                            
        <v-card class="white--text card-info">
            <v-card-media
            v-bind:src="product.avatar_url"
            height="130px"
            cover
            >
            </v-card-media>
            <v-card-title primary-title>
                <div class="headline"><h4 class="item-title">{{appendTitle(product.item_name)}}</h4></div>
                <v-spacer></v-spacer>
                <span class="item-price">R$ 1.099,99</span>
            </v-card-title>

        </v-card>
    </v-flex>
</template>

<script>
export default {
  name: 'ProductCard',
  props: ['product'],
  methods: {
    appendTitle: function(title){
        if (title.length < 30) {
            return title
        }else{
            return title.substring(0,30)+' ...'
        }
    }
  }
}
</script>

<style>
    .card-box{
        cursor: pointer;
        margin-left: auto;
        margin-right: auto;
        margin-top: 10px;
        margin-bottom: 20px; 
        width: 190px;
    }
    .card-info{
        min-height: auto;
        max-height: initial;
        min-width: 100%;       
    }
    .card__title--primary.primary-col {
        padding-top: 17px;
        min-height: 80px;
        max-height: 80px;
        text-align: left!important;
        display: inline-table;
        box-sizing: content-box;
        float: left;
        width: 90%;
    }
    .card__title--primary {
        padding: 10px;
    }
    .item-title {
        font-size: 14px;
        font-weight: 100;
        text-align: left;
        justify-content: left;
        line-height: 17px;
        color: #000;
    }
    .item-price {
        color: #17a2b8;
        width: 100%;
        text-align: left;
        padding-top: 8px;
        font-weight: 300;
        font-size: 14px;
    }
    
    .card__media .card__media__background {
        width: 100%;
    }    
    .card__media {
        background: #fff;
        border-radius: 0;
        width: 60%;
        margin-left: auto;
        margin-right: auto;
        margin-bottom: 0px;
        margin-top: 0px;              
    }     
    .card__title--primary.primary-col {
        padding-top: 17px;
        min-height: 80px;
        max-height: 80px;
        text-align: left!important;
        display: inline-table;
        box-sizing: content-box;
        float: left;
        width: 90%;
    }
    .card__title--primary {
        padding: 10px;
    }
    .card__actions {
        display: block;
        padding: 0;
    }
    .card__media__content {
        display: none;
    }
    .card__actions .btn, .card__actions>* {
        margin: 0px 0px 3px 0px;
        font-size: 11px;
        line-height: 7px;
        width: 95%;
    }    
    .card {
        border-radius: 5px;
        padding: 5px;
        box-shadow: 0 2px 1px -1px rgb(0 0 0 / 10%), 0 1px 1px 0 rgb(0 0 0 / 0.1), 0 1px 3px 0 rgba(0,0,0,.1);
    }
    .card__media__content {
        display: none;
    }        
</style>