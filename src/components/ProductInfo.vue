<template>
    <v-navigation-drawer
        temporary
        :right="right"
        v-model="rightDrawer"
        fixed
        app
        class="aside-open"
        width=500
    >
        <v-list two-line subheader>
            <v-progress-circular indeterminate color="primary" class="loading"></v-progress-circular>
            <p class="loading-p">Carregando informações</p>
            <!-- {{dataInfo}} -->
            <div class="request-box">
                <v-list-tile v-for="request in requests" :key="request.id" avatar class="hr-bottom" v-bind:href="request.html_url"  target="_blank">
                    <v-list-tile-avatar>
                        <img :src="request.user.avatar_url">
                    </v-list-tile-avatar>
                    <v-list-tile-content>
                        <v-list-tile-title>{{request.title}}</v-list-tile-title>
                        <v-list-tile-sub-title>{{request.body}}</v-list-tile-sub-title>
                    </v-list-tile-content>
                    <v-subheader>{{dateString(request.created_at)}}</v-subheader>                    
                </v-list-tile>              
            </div>
        </v-list>
    </v-navigation-drawer>   
</template>

<script>
export default {
  name: 'ProductInfo',
  props: ['dataInfo'],
//   components: {},
  data () {
    return {
        right: true,
        rightDrawer: false,
        requests: '',        
    }
  }    
}
</script>

<style>
    .loading{
        width: 100%!important;
        margin-top: 40px;
        text-align: center
    }
    .subheader--inset {
        margin-left: 0;
        background: #307bf5;
        color: #fff!important;
        padding-left: 15px;
    }
    .loading-p {
        text-align: center;
        padding-top: 14px;
        font-weight: 600;
    }
    .list.list--subheader.list--two-line {
        margin-top: 45%;
    }    
    /* .subheader--inset #close-box{
        padding-right: 5px;
        margin-right: 5px;
        height: 100%;
        outline: none
    }         */
</style>