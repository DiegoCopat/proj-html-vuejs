<template>
  <header>
      <section class="wrapper">

          <!-- NAVBAR SECTION -->
          <section class="navbar">
              <div class="left">
                  <img src="../assets/images/takeout-logo.png" alt="logo">
              </div>
              <div class="right">
                  <ul>
                      <li v-for="(elementMenu, index) in menu" :key="index">{{ elementMenu.nome }}</li>
                  </ul>
              </div>
          </section> <!-- /NAVBAR SECTION -->
      </section>
  </header>
</template>

<script>
export default {
    name: "Header",
    data: function() {
        return {
            menu: [
                {
                    nome: "Home"
                },
                {
                    nome: "Order Online"
                },
                {
                    nome: "About"
                },
                {
                    nome: "News"
                },
                {
                    nome: "Contact Us"
                },
                {
                    nome: ""
                }
                
            ]
        }
    }
}
</script>

<style lang="scss" scope>
    header {
        width: 100%;
        height: 800px;
        background-image: url(../assets/images/home-background-hero-scaled.jpg);
        background-size: cover;
        background-position: bottom center;

        .navbar {
            display: flex;
            width: 100%; 
            height: 100px; 
            background-color: black;
            padding-top: 30px;

            .left {
                display: flex;
                width: 50%;
                height: 100%;

                img {
                    width: 45%;
                    margin: auto 0;
                }
            }

            .right {
                width: 50%;
                height: 100%;
                border: 1px solid white;
                color: white;

                ul {
                    display: flex;
                    height: 100%;
                    

                    li {
                        margin: auto;
                        list-style: none;
                        font-weight: 700;
                    }
                }
            }

        }

    }
</style>