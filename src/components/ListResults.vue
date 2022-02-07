<template>
    <div class="list-result">
        <div class="loader-box">
            <!-- <h4 class="header-list-title">Todos os repositórios desenvolvidos em JAVA</h4> -->
            <v-card class="category-card">
                <v-container
                    fluid
                    style="min-height: 0;"
                    grid-list-lg
                >
                    <div class="row"><h2>Açougue</h2></div>
                    <!-- <v-layout row wrap class="dash-list" v-bind:key="source.id" v-for="source in sources"> -->
                    <v-layout row wrap class="dash-list" v-bind:key="demo.id" v-for="demo in demos">                        
                        <!-- <v-flex xs12 class="card-box"  @click.stop="rightDrawer = !rightDrawer; getRequests(demo.owner.login,demo.name)"> -->
                        <ProductCard :demo="demo"/>
                    </v-layout>
                </v-container>
            </v-card>
        </div>                      
    </div>
</template>

<script>
import ProductCard from '@/components/ProductCard';

export default {
    name: 'list-results',
    components: {
        ProductCard
    },
    data () {
        return{
            // sources: [],
            // source: '',
            // requests: [],
            demos: [
                {
                    'id': 0,
                    'cat_name': 'Promoções',
                    'item_name': 'Guaraná Antártica 350ml',
                    'avatar_url': 'https://emporiodacerveja.vtexassets.com/arquivos/ids/167393-232-232?width=232&height=232&aspect=true',
                    'delivery_price': 'R$ 1.099,90',
                    'shipping_price': 'R$ 999,90'
                },
                {
                    'id': 1,
                    'cat_name': 'Promoções',
                    'item_name': 'Guaraná Antártica 350ml',
                    'avatar_url': 'https://emporiodacerveja.vtexassets.com/arquivos/ids/167393-232-232?width=232&height=232&aspect=true',
                    'delivery_price': 'R$ 1.099,90',
                    'shipping_price': 'R$ 999,90'
                },
                {
                    'id': 2,
                    'cat_name': 'Promoções',
                    'item_name': 'Guaraná Antártica 350ml',
                    'avatar_url': 'https://emporiodacerveja.vtexassets.com/arquivos/ids/167393-232-232?width=232&height=232&aspect=true',
                    'delivery_price': 'R$ 1.099,90',
                    'shipping_price': 'R$ 999,90'
                },
                {
                    'id': 3,
                    'cat_name': 'Promoções',
                    'item_name': 'Guaraná Antártica 350ml',
                    'avatar_url': 'https://emporiodacerveja.vtexassets.com/arquivos/ids/167393-232-232?width=232&height=232&aspect=true',
                    'delivery_price': 'R$ 1.099,90',
                    'shipping_price': 'R$ 999,90'
                },
                {
                    'id': 4,
                    'cat_name': 'Promoções',
                    'item_name': 'Guaraná Antártica 350ml',
                    'avatar_url': 'https://emporiodacerveja.vtexassets.com/arquivos/ids/167393-232-232?width=232&height=232&aspect=true',
                    'delivery_price': 'R$ 1.099,90',
                    'shipping_price': 'R$ 999,90'
                },
                {
                    'id': 5,
                    'cat_name': 'permalink',
                    'item_name': 'Ver todos',
                    'avatar_url': 'promo-all',
                    'delivery_price': '',
                    'shipping_price': ''
                }                                                                                 
            ]                        
        }
    },
    methods: {
        getRequests: function (owner,repo,desc){
            document.querySelector('.request-box').style.display = 'none'
            document.querySelector('.loading').style.display = 'inline-block';
            this.$http.get('https://api.github.com/repos/'+owner+'/'+repo+'/pulls')
            .then(response => {
                this.requests = response.body 
                console.log(response.body)
            })
            .then(function(){
                document.querySelector('.loading').style.display = 'none';
                document.querySelector('.request-box').style.display = 'block'
            })
        },
        dateString: function(date){
            var date_t = date.split('T'),
                exit_date = date_t[0].split('-')
            return ''+exit_date['2']+'/'+exit_date['1']+''
        },
        appendSubstring: function(substrin){
            if (substrin.length < 90) {
                return substrin
            }else{
                return substrin.substring(0,90)+' ...'
            }
        }        
    },
    created: function() {
        this.$http.get('https://api.github.com/search/repositories?q=language:java')
        .then(response => {
            this.sources = response.body.items
            console.log(response.body.items)
        })
        .then(function(){
            document.querySelector('.dash-loading').style.display = 'none'
            document.querySelector('.full-loading').style.display = 'none'
            document.querySelector('.loader-box').style.display = 'block'
        })
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
