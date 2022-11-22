<script>
export default{
    name: "AppMainTopHalf",
}

</script>


<template>
<section class="main_logistic">
    <div class="container">
        <div class="flex">
            <div class="info">
                <p class="blu-p">our business areas</p>
                <h2>Logistics Services</h2>
                <p>we are leaders in providing logistics services with a set of cutting edge technologies and team of experienced and renowned professionals.</p>
                 
            </div>
            <div class="card">
                <img src="../assets/img/gallery-3.jpg" alt="">
                <h3>Technology</h3>
                <p>Focused on developing technology solutions adapted to our client's needs.</p>
            </div>
            <div class="card">
                <img src="../assets/img/gallery-5.jpg" alt="">
                <h3>Transport</h3>
                <p>We develop operational strategies to improve logistical efficiency.</p>
            </div>
        </div>
    </div>
</section>

<section class="main_company">
        <div class="flex">
            <div class="split">
                <p class="blu-p">about the network</p>
                <h2><span class="blu-shadow">The</span> Company</h2>
            </div>
            <div class="split">
                <img src="../assets/img/about-5.jpg" alt="">
            </div>
        </div>
</section>

<section class="main_tag">
    <div class="container">
        <div class="flex">
            <img src="../assets/img/logo-5.png" alt="">
            <img src="../assets/img/logo-1.png" alt="">
            <img src="../assets/img/logo-2.png" alt="">
            <img src="../assets/img/logo-3.png" alt="">
            <img src="../assets/img/logo-4.png" alt="">
            <img src="../assets/img/logo-5.png" alt="">
        </div>
    </div>

</section>
</template>


<style lang="scss" scoped>
@use "../assets/style/partials/variables" as *;
@use "../assets/style/general.scss" as *;

img{
    
}

.main_logistic,
.main_tag{
    background-color: $bg-main-lightgreen;
    padding: 4rem 0 ;
}
.flex{
    justify-content: space-between;
    
    .info,
    .card{
        width: calc(100% / 3 - 15px);
    }
    .card{
        background-color: $primary-font-white;
        padding: 2rem 3.5rem;
        h3{
            margin: 1rem 0;
        }
    }
}


.main_company{
    background-color: $bg-dark;
    .container{
        
    }
    .split{
        width: calc(100% / 2);
        text-align: end;
        color: $primary-font-white;
    }
}
.main_tag img{
   
}
</style>