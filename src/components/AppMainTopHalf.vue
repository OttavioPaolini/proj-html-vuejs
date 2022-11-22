<script>
export default{
    name: "AppMainTopHalf",


    data(){
        return{

            
        }
    }
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

                <a class="btn btn-p" href="">read more</a>
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
    <div class="container">
        <div class="flex">
            <div id="test" class="split flex">
                <div class="text">
                    <p class="blu-p">about the network</p>
                    <h2><span class="blu-shadow">The</span> Company</h2>
                    <p>With all of this expertise and capability comes an unrivalled commitment to customer service.</p>
                    <ul>
                        <li>
                            <div class="box-sx">
                                <small class="circle">
                                    <span class="bigger">0</span>
                                    <span>%</span>
                                </small>
                            </div>
                            <div class="box-dx">
                                <h4>Leadership</h4>
                                <p>lorem ipsum va bene anche se scrivo altro</p>
                            </div>
                        </li>


                        <li>
                            <div class="box-sx">
                                <small class="circle">
                                    <span class="bigger">0</span>
                                    <span>%</span>
                                </small>
                            </div>
                            <div class="box-dx">
                                <h4>Leadership</h4>
                                <p>lorem ipsum va bene anche se scrivo altro</p>
                            </div>
                        </li>


                        <li>
                            <div class="box-sx">
                                <small class="circle circle-b">
                                    <span class="smaller">1</span>
                                    <span>%</span>
                                </small>
                            </div>
                            <div class="box-dx">
                                <h4>Leadership</h4>
                                <p>lorem ipsum va bene anche se scrivo altro</p>
                            </div>
                        </li>
                    </ul>
                </div>
            </div>
            <div class="split split-dx">
                <!-- <img id="img" src="../assets/img/about-5.jpg" alt=""> -->
            </div>
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



.main_logistic,
.main_tag{
    background-color: $bg-main-lightgreen;
    padding: 4rem 0 ;
}
.main_tag{
    img{
        height: 30px;
        filter: grayscale(20%);
    }

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
    
#img{
    height: 100%;
}
    .split{
        width: calc(100% / 2);
        text-align: end;
        color: $primary-font-white;
       &-dx{
        background-image: url("../assets/img/about-5.jpg");
        background-size: cover;
        background-position: center;
       }
        .text{
            width: 50%;
            text-align: left;
            padding: 5rem 0;
            font-size: 1.2rem;
            
            p{
                font-weight: 200;
                padding: 1rem 0;
            }
            li{
                display: flex;
                margin: 1rem 0;

                .box-sx{
                    width: 25%;
                    display: flex;
                    justify-content: start;

                    .bigger{
                        font-size: 1.5rem;
                    }
                    .smaller{
                        font-size: 1.5rem;
                    }

                    .circle{
                        display: inline-block;
                        width: 50px;
                        height: 50px;
                        border: 3px solid grey;
                        border-radius: 50%;
                        line-height: 50px;
                        text-align: center;  
                    }
                    .circle-b{
                        
                    }
                }
                .box-dx{
                    width: 75%;
                    
                }
            }
        }
    }
}
#test{
    // justify-content: end;
}
</style>