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
}
</script>


<template>
<section>
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
        </div>
        <div class="transport">
            <h3>Transport</h3>
        </div>
        <div class="support">
            <h3>Support</h3>
        </div>
    </div>

</section>


</template>


<style lang="scss" scoped>
@use "../assets/style/general.scss" as *;
@use "../assets/style/partials/variables" as *;

section{
    background-image: url("../assets/img/bg-10.jpg");
    height: 500px;
    background-position: center;
    background-size: cover;

    h3{
        color: $primary-font-white;
    }
}

</style>