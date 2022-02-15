<template>
    <div class="list-result">
        <div class="loader-box">
            <v-card class="category-card">
                <v-container
                    fluid
                    style="min-height: 0;"
                    grid-list-lg
                >
                    <div class="row"><h2>Açougue</h2></div>
                    <v-layout row wrap class="dash-list" v-bind:key="product.id" v-for="product in products" @click="handleSelectItem(product)">                        
                        <ProductCard :product="product" />
                    </v-layout>
                </v-container>
            </v-card>
        </div>
        <div>
            <ProductInfo :dataInfo="dataInfo" />
        </div>
    </div>
</template>

<script>
import ProductCard from '@/components/ProductCard';
import ProductInfo from '@/components/ProductInfo';

import products from '@/data/products.json';

export default {
    name: 'list-results',
    components: {
        ProductCard,
        ProductInfo
    },
    data () {
        return{
            products,
            dataInfo: ''
        }
    },
    created: function() {
        this.$http.get()
        .then(function(){
            document.querySelector('.dash-loading').style.display = 'none'
            document.querySelector('.full-loading').style.display = 'none'
            document.querySelector('.loader-box').style.display = 'block'
        })
    },
    methods: {
        handleSelectItem(item){
            this.dataInfo = item;
            alert(item.item_name)
        }
    }
}
</script>

<style scoped>
    body{
        background: #fafafa
    }
    .category-card {
        margin-bottom: 20px;
        box-shadow: none!important;
    }
    .container.fluid.grid-list-lg {
        text-align: center;
        padding: 0
    }
    .layout.dash-list.row.wrap{
        margin: 0;
        display: inline-block;        
    }
    .category-card h2 {
        color: #17a2b8;
        text-transform: uppercase;
        font-weight: 400;
        font-size: 15px;
        text-align: left;
        padding: 7px 0 0 12px;
    }
    /* .owner-title{text-align:center} */
    /* .list-col{display: inline-block;text-align:center}
    .list-col .avatar{margin-left: auto;margin-right: auto} */
    /* .subheader--inset {
        margin-left: 0;
        background: #307bf5;
        color: #fff!important;
        padding-left: 15px;
    } */
    /* .subheader--inset #close-box{
        padding-right: 5px;
        margin-right: 5px;
        height: 100%;
        outline: none
    } */
    /* .hr-bottom{
        border-bottom: 1px solid #ccc!important
    } */
    .header-list-title {
        text-align: center;
        padding: 30px;
        padding-top: 0;
    }
    .source-selection {
        display: table;
    }
    .toolbar__title {
        width: 100%;
        text-align: center;
    }
    .loading{
        width: 100%!important;
        margin-top: 40px;
        text-align: center
    }
    .loader-box{
        display: none
    }
    .btn .icon--left {
        margin-right: 0px;
    }
    .btn--flat {
        background-color: red;
    }    
    .btn .icon--left {
        margin-right: 8px;
        font-size: 16px;
    }
    .btn__content {
        font-size: 11px;
        line-height: 5px;
    }
    .item-add {
        border-radius: 5px;
        color: #fff!important;                
    }
    .btn-delivery {
        background: #17a2b8!important;
    }
    .btn-wish {
        background: #34a853!important;
    }
    @media only screen and (min-width: 1367px) {
        .layout.dash-list.row.wrap{
            width: 16%;
            transform: translateX(-2%);
        }
    }    
    @media only screen and (min-width: 1024px) and (max-width: 1366px) {
        .layout.dash-list.row.wrap{
            width: auto
        }
    }
    @media only screen and (min-width: 768px) and (max-width: 1023px) {
        .layout.dash-list.row.wrap{
            width: 24%
        }
    }    
</style>
