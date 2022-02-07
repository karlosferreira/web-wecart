<template>
    <div class="shipping-box">
        <v-text-field
            value="Rua Soldado Jacinto Costa, 22"
            label="Endereço para entregas"
            outlined
            readonly
            class="input-read"
        ></v-text-field>
    </div>  
</template>

<script>
export default {
  name: 'ShippingBox',
//   components: {},
//   data () {
//     return {}
//   }  
}
</script>

<style>
  .shipping-box {
    display: flex;
    width: 260px;
    margin-right: auto;
    transform: translateY(-5px);
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