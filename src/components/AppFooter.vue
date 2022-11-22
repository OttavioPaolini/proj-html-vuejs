<script>
import AppLogo from './AppLogo.vue';

export default {
    name: "AppFooter",

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
            footerList:[   
            ["The Company", "Institutional", "Social & Events", "Innovation", "Environment", "Technology"],     
            ["Industrialized", "Chemicals","Package Liquids", "Construction", "Laminated Wood", "And others"],   
            ["Responsibility", "Term of Use", "About Cookies", "Privacy Policy", "Accessibility", "Information"]
            ]
        
    }
}}
</script>


<template>
<section class="flex">
    <div class="container flex">
        <div class="contact">
            <AppLogo />
            <p>A Functional HTML Template for Corporate & Business.</p>
            <a href="">
                    <i class="fa-solid fa-phone"></i>
                    {{number}}
                </a>
                <a href="">
                    <i class="fa-solid fa-envelope"></i>
                    {{mail}}
                </a>
                <a href="">
                    <i class="fa-solid fa-location-dot"></i>
                    {{gps}}
                </a> 
                
                <a href="" class="btn btn-s">get in touch</a>
        </div>
        <div class="about">
            <h3>About</h3>
            <ul>
                <li v-for="(items, index) in footerList[0] "><a href="">{{items}}</a></li>
            </ul>
        </div>
        <div class="transport">
            <h3>Transport</h3>
            <ul>
                <li v-for="(items, index) in footerList[1] "><a href="">{{items}}</a></li>
            </ul>
        </div>
        <div class="support">
            <h3>Support</h3>
            <ul>
                <li v-for="(items, index) in footerList[2] "><a href="">{{items}}</a></li>
            </ul>
        </div>
    </div>

</section>


</template>


<style lang="scss" scoped>
@use "../assets/style/general.scss" as *;
@use "../assets/style/partials/variables" as *;

section{
    background-image: url("../assets/img/bg-10.jpg");
    // height: 500px;
    background-position: center;
    background-size: cover;
    font-weight: 100;
    color:$primary-font-white;
    .container{
        justify-content: space-between;
        margin: 5rem auto;
        
        h3{
            font-size: 1.5rem;
            color: $primary-font-white;
        }
        li a::before{
            content: ">";
            display: inline-block;
            margin-right: 10px;
        }
        .about,
        .transport,
        .support{
            background-color: rgba($color: white, $alpha: .1);
            border-radius: 10px;
            
        }
        .contact,
        .about,
        .transport,
        .support{
            width: calc(100% / 4 - 30px);
            padding: 2rem;
            *{
                margin: 1rem 0;
            }
        }
    }
}

</style>