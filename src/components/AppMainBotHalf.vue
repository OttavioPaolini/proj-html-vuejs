<script>
export default{
    name: "AppMainBotHalf",

    props:{
        number: String,
        mail: String,
        gps: String,
    },
    data(){
        return{

        }
    }

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
        <div class="flex">
            <div class="cards cards-a">
                <div class="opacity-layer flex">
                    <h3>Increasing creativity is possible for everyone</h3>
                </div>
            </div>
            <div class="cards cards-b">
                <div class="opacity-layer flex">
                    <h3>Because market research is part of the business plan</h3>
                </div>
            </div>
            <div class="cards cards-c">
                <div class="opacity-layer flex">
                    <h3>Working from home is now a trend</h3>
                </div>
            </div>
        </div>
    </div>
</section>
<section class="main-newsletter">
    <div class="container-xs flex">
        <div class="split">
            <div class="text">
                <p class="blu-p">newsletter</p>
                <h3><span class="blu-shadow">Know</span> First</h3>
                <p>Follow closely and receive content about our company and the news of the current market.</p>
            </div>
        </div>
        <div class="split">
            <div class="form">
                
                <input type="text" id="Name" name="Name" placeholder="Name">
                
                <input type="text" id="mail" name="mail" placeholder="Email">
            </div>
            <a href="" class="btn btn-p">subscribe</a>
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
                <div class="left">
                    <input type="text" id="fname" name="firstname" placeholder="Name">
                    <input type="num" id="phone" name="phone" placeholder="Phone">
                </div>
                <div class="right">
                    <input type="mail" id="mail" name="mail" placeholder="Email">
                    <select id="more" name="more">
                        <option value="">More info</option>
                        <option value="2">2</option>
                        <option value="3">3</option>
                    </select>
                </div>
                <textarea name="message" id="message" cols="30" rows="10" placeholder="Message"></textarea>
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

    .cards{
        margin-top: 2rem;
        height: 350px;
        background-size: cover;
        width: calc(100% / 3 - 20px);
        border-radius: 15px;
        .opacity-layer{
            border-radius: 15px;
            text-align: center;
        }
        h3{
            align-self: flex-end;
            color:$primary-font-white;    
            padding: 2rem;
        }
       &-a{
        background-image: url("../assets/img/news-1.jpg");
       }
       &-b{
        background-image: url("../assets/img/news-2.jpg");
       }
       &-c{
        background-image: url("../assets/img/news-3.jpg");

       }
    }
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
    .container-xs{
        height: 100%;
        
        
        .split{
        width: calc(100% / 2 - 20px);

        .text {
            padding:3rem;
            h3{
                margin: 1rem 0;
            }
        }
        .btn{
            margin: 1rem 0;
        }
        input{
            width: 100%;
            margin: 5px 0;
            padding: .8rem;
            border: none; 
            background-color: lightgray;

        }
        
    }
    }

}





// MAIN-CONTACT-STYLE

.main-contact{
    background-color: $bg-main-lightgreen;
    padding: 4rem 0 ;

    .col-form{
        width: 70%;

        textarea{
            height: 200px;
            resize: none;
            width: 100%;
            display: block;
            margin-bottom: 2rem;
            border: none;
            padding: .8rem;
            background-color: lightgray;
            
        }
        .left,
        .right{
          ;
            input,
            select{
                width: calc(100% / 2 - 10px);
                margin:5px 5px 10px 0;  
                padding: .8rem;
                border: none; 
                background-color: lightgray;             
            }
        }

    }
    .col-example{
        width: 30%;
        padding: 0 2rem;

        a:not(:last-child){
            padding: 1rem 0;
            color:$dark-acqua;
            display: block;

            i{
                background-color: rgba($color: $light-acqua, $alpha: .3);
                padding: .8rem;
                border-radius: 50%;
            }
        }
        .btn-s{
            color: $dark-acqua;
        }
    }
}
</style>