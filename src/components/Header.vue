<template>
    <header>
        
        <!-- NAVBAR SECTION -->
        <section class="navbar">
            <div class="container">
                <div class="left">
                <img src="../assets/images/takeout-logo.png" alt="logo">
                </div>
                <div class="right">
                    <ul>
                        <li v-for="(elementMenu, index) in menu" :key="index" :class="elementMenu.active ? 'active' : ''" >
                            <a href="">
                                {{ elementMenu.nome }} 
                                <i v-if="elementMenu.active == true" class="fas fa-chevron-down"></i>
                            </a> 
                            
                        </li>
                        <li>
                            <a href=""><i class="fas fa-shopping-cart"></i></a>
                        </li>
                    </ul>
                </div>
            </div>

        </section> <!-- /NAVBAR SECTION -->

        <!-- JUMBOTRON SECTION -->
        <section class="wrapper">    
            <section class="jumbotron"> 
                <div class="text-1">Hungry?</div>
                <h2 class="text-2">Great Food</h2>
                <h3 class="text-3">Delivered</h3>
                <button class="button-1">
                    View our menu
                    <i class="fas fa-arrow-circle-right"></i>
                </button>
                <section class="services">
                    <div class="option">
                        <i class="far fa-clock"></i>
                        24/7 delivery
                        </div>
                    <div class="option">
                        <i class="fas fa-hamburger"></i>
                        over 100 dishes
                        </div>
                    <div class="option">
                        <i class="fas fa-mobile-alt"></i>
                        in app ordering
                        </div>
                    <div class="option">
                        <i class="fas fa-car"></i>
                        fast delivery
                        </div>
                </section>
            </section>
        </section> <!-- /JUMBOTRON SECTION -->
    </header>
</template>

<script>
export default {
    name: "Header",
    data: function() {
        return {
            menu: [
                {
                    nome: "Home",
                    active: true
                },
                {
                    nome: "Order Online",
                    active: false
                },
                {
                    nome: "About",
                    active: false
                },
                {
                    nome: "News",
                    active: false
                },
                {
                    nome: "Contact Us",
                    active: false
                }
                
            ],
            currentActive: ""
        }
    },
    methods: {
        getUserActive: function(element, index) {
            console.log(element, index);
        }

        
    }
}
</script>

<style lang="scss" scope>
@import "../style/graphics.scss";
@import "../style/colors.scss";

    header {
        display: flex;
        width: 100%;
        height: 800px;
        background-image: url(../assets/images/home-background-hero-scaled.jpg);
        background-size: cover;
        color: $white;
        background-position: bottom center;

            .navbar {
                display: flex;
                position: fixed;
                width: 100%; 
                height: 100px; 
                padding: 30px 0 30px 0;
                background-color: rgba($marshland, 0.4);
                z-index: 2;

                .container {
                    display: flex;
                    width: 60%; 
                    height: 100%;
                    margin: auto;
                }
                .left {
                    display: flex;
                    width: 50%;
                    height: 100%;
                    margin: auto;

                        img {
                            width: 45%;
                            margin: auto 0;
                        }
                }

                .right {
                    width: 50%;
                    height: 100%;
                    color: $white;

                    ul {
                        display: flex;
                        height: 100%;
                        
                        li {
                            margin: auto;
                            list-style: none;
                            font-size: 12px;
                            font-weight: 700;

                            a{
                                text-decoration: none;
                                color: $white;
                            }
                        }
                    }
                }
            }
            .jumbotron {
                width: 100%; 
                height: 200px;
                margin: auto;
                // border: 1px solid $white;
                button i{
                    margin-left: 5px;
                }
                button:hover {
                    cursor: pointer;
                }

                h3 {
                    margin-bottom: 20px;
                }
                
                .services {
                    display: flex;
                    width: 100%;
                    height: 80px;
                    background-color: $white;
                    position: absolute; 
                    bottom: -55px;
                    // justify-content: space-around;

                    .option {
                        width: 20%;
                        font-size: 11px;
                        font-weight: 600;
                        color: $marshland;
                        text-transform: uppercase; 
                        text-align: center;
                        margin: auto;
                        
                        i {
                            margin-right: 6px;
                        }
                    }
                }
            }
        }
    
</style>