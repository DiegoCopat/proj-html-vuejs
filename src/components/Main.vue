<template>
  <main>
        <section class="wrapper">
            <section class="top">
            <h2>Our Most Popular Dishes</h2>
            <section class="dishes">
                <!-- <div class="product"> 
                    <Card 
                    v-for="(product, index) in products" :key="index" :singularProduct="product"/>
                </div> -->
                <div class="card"></div>
                <div class="card"></div>
                <div class="card"></div>
            </section>
            <button class="button-1">
                        Start your order
                        <i class="fas fa-arrow-circle-right"></i>
                    </button>
        </section>
        <section class="center"></section>
        <section class="bottom"></section>
        </section>
    
  </main>
</template>

<script>
import Products from "../data/Products";
// import Card from "./Card";

export default {
    name: "Main",
    components: {
        // Card
    },
    data: function() {
        return {
            products: Products
        }
    }
}
</script>


<style lang="scss" scope>
@import "../style/graphics.scss";
@import "../style/colors.scss";

    Main {
        width: 100%;
        height: 100vh;
        background-color: $white;
        padding-top: 100px;
        text-align: center;

        .top {
            width: 100%;

            h2 {
                font-size: 30px;
                font-weight: 800;
            }

            .dishes {
                display: flex;

            .card {
                width: calc(100% / 3.1);
                height: 200px;
                margin: auto;
                background-color: green;
                border: 1px solid white;

            }
        }
        }
        
        
    }
</style>