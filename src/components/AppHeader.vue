<script>
export default{
    name: "AppHeader",
    props:{
        number: String,
        mail: String,
        gps: String,
    }
}
</script>

<template>
    <!-- header-fixed -->
    <section class="header-fixed">
        <div class="container">
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
    <section class="header-nav">
        <img src="../assets/img/jumbo.jpg" alt="">
        <div class="container">

        </div>
    </section>

</template>

<style lang="scss" scoped>
@use "../assets/style/partials/variables" as *;

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


// HEADER-NAV-CSS



</style>