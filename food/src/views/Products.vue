<template>
    <div class="container" v-if="products">
        <div class="card" v-for="product in products" :key="product.id"  style="width: 18rem;">
         <img class="card-img-top" :src="product.image" alt="Card image cap">
        <div class="card-body">
          <h5 class="card-title">{{product.title}}</h5>
        <p class="card-text">{{product.price}} €</p>
        <button @click="addToCart(product)" class="btn btn-primary">ajouter au panier</button>
  </div>
</div>
    </div>
  
</template>

<script>
export default {
    created(){
        this.$store.dispatch("getProducts");
    },
    computed:{
        products(){
            return this.$store.state.products;
        }
    },
    methods:{
        addToCart(product){
            this.$store.dispatch("addToCart",product).then(()=>{
                console.log(this.$store.state.cart);
            })
        }
    }

}
</script>

<style scoped lang="scss">
  .container{
      display: flex;
      justify-content: space-between;
      flex-wrap:wrap;
     
        .card{
          margin: 10px;
          height: 500px;
         
            img{
              max-width:200px;
              padding: 50px;
            }
        }
    }
</style>
