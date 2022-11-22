<script>
export default{
    name: "AppMainBotHalf",

    props:{
        number: String,
        mail: String,
        gps: String,
    },

}
</script>


<template>
<section class="main-news">
    <div class="container">
        <p class="blu-p">our editorial content</p>
        <h2>Latest <span class="blu-shadow blu-shadow-text">News</span></h2>
        <div class="flex">
            <p>Every week publish content about what is best in the business world.</p> 
            <span class="btn btn-p"><a href="">see all</a></span>
        </div>
    </div>
</section>
<section class="main-newsletter">
    <div class="container-s flex">
        <div class="split">
            <div class="text">
                <p class="blu-p">newsletter</p>
                <h3><span class="blu-shadow">Know</span> First</h3>
                <p>Follow closely and receive content about our company and the news of the current market.</p>
            </div>
        </div>
        <div class="split">
            <div class="form">
                <label for="Name"></label>
                <input type="text" id="Name" name="Name" placeholder="Name">
                <label for="mail"></label>
                <input type="text" id="mail" name="mail" placeholder="Email">
                <a href="" class="btn btn-p">subscribe</a>
            </div>
        </div>
    </div>
</section>
<section class="main-contact">
    <div class="container">
        <div class="flex">
            <div class="col-form">
                <p class="blu-p">send a message</p>
                <h3>Get in <span class="blu-shadow blu-shadow-text">Touch</span></h3>
                <p>We will respond to your message ASAP.</p>
                <a href="" class="btn btn-p">send</a>
            </div>
            <div class="col-example">
                <h4>Example Inc.</h4>
                <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Repellendus repudiandae dignissimos laudantium, quam doloribus nihil aliquam harum. Impedit mollitia repellendus consectetur dolorum! Possimus, rerum neque. In tempora a similique reprehenderit?</p>
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
                
                <a href="" class="btn btn-s">view map</a>
            </div>        
        </div>
    </div>
</section>
</template>

<style lang="scss" scoped>
@use "../assets/style/general.scss" as *;
@use "../assets/style/partials/variables" as *;

// MAIN-NEWS-STYLE
.main-news{
    margin: 5rem 3rem;
}
.flex{
    justify-content: space-between;
    align-items: center;
}
    

// MAIN-NEWSLETTER-STYLE
.main-newsletter{
    background-image: url("../assets/img/bg-1.jpg");
    background-position: center;
    background-size: cover;
    height: 350px;
    .text{
        color: $primary-font-white;
        
    }
    .container-s{
        height: 100%;
        
        .split{
        width: calc(100% / 2);
        
    }
    }
}

// MAIN-CONTACT-STYLE

.main-contact{
    background-color: $bg-main-lightgreen;
    padding: 4rem 0 ;

    .col-form{
        width: 70%;
    }
    .col-example{
        width: 30%;

        a{
            padding: 1rem 0;
            color:$dark-acqua;
            display: inline-block;
        }
    }
}
</style>