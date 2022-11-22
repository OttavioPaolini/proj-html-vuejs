<script>
import AppLogo from './AppLogo.vue';
export default{
    name: "AppHeader",

    components:{
        AppLogo,
    },

    props:{
        number: String,
        mail: String,
        gps: String,
    },
    data(){
        return{
            menu: ["home", "service", "skills", "partners", "blog"]

            
        }
    }
}
</script>

<template>
    <!-- header-fixed -->
    <section class="header-fixed">
        <div class="container flex container-100">
            <div class="header-fixed__daily">
                <i class="fa-solid fa-clock"></i>
                <span class="pl-1">Open Hours: Mon - Sat - 9:00 - 18:00</span>
            </div>
            <div class="header-fixed__info">
                
                <span>
                    <i class="fa-solid fa-phone"></i>
                    {{number}}
                </span>
                <span>
                    <i class="fa-solid fa-envelope"></i>
                    {{mail}}
                </span>
                <i class="fa-brands fa-facebook"></i>
                <i class="fa-brands fa-twitter"></i>
                <i class="fa-brands fa-linkedin"></i>
            </div>
        </div>
    </section>

    <!-- navbar-section -->
    <section class="header">
        <div class="opacity-layer">
            <div class="container flex">
                <div>
                    <AppLogo />
                </div>
                <ul class="navbar">
                    <li v-for="(item, index) in menu" :key="index"><a href="">{{item}}</a></li>
                    <li ><a class="btn btn-p" href="">get in touch</a></li>
                </ul>

            </div>
            <div class="container-jumbo flex">
                <div class="container-jumbo-text">
                    <h1>Logistics that goes further.</h1>
                    <p>For 20 years working with the most innovative in the field of transport.</p>
                    <a class="btn btn-p" href="">get in touch</a>
                    <a class="btn btn-s" href="">read more</a>
                </div>
            </div>
        </div>
    </section>

</template>

<style lang="scss" scoped>
@use "../assets/style/partials/variables" as *;
@use "../assets/style/general.scss" as *;

// HEADER-FIXED-CSS
.header-fixed{
    background-color: $bg-header-fixed;
    height: 40px;
    color: $secondary-font-grey;
    .container{
        justify-content: space-between;
        align-items: center;     
    }
    &__info *{
        padding-left: 1rem;
    }
}


// HEADER-CSS
.header{
    background-image: url("../assets/img/jumbo.jpg");
    background-position: left bottom;
    background-repeat: no-repeat;
    background-size: cover;
    width: 100%;

    // debug
    height: 500px;
    .opacity-layer{
        height: 100%;
        background: rgba($color: #000000, $alpha: .4);
    }
    .container{
        justify-content: space-between;
        padding-top: 2rem;

        ul{
            display: flex;
            color: $primary-font-white;
            font-size: 1rem;
            text-transform: uppercase;
            li{
                display: inline-block;
                margin-left: 2rem;
            }
        }

        &-jumbo{
            width: 80%;
            max-width: 1120px;
            margin: 0 auto;
            justify-content: end;
            &-text{
                margin-top: 5rem;
                color: $primary-font-white;
                font-weight: 200;
                a{
                    margin-right: .5rem;
                }
                h1{
                    font-size: 3.5rem;
                                      
                }
                width: 30%;

                div{
                    width: 20%;
                }
            }
        }
    }
}



</style>