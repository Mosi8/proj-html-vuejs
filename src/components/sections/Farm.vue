<template>
    <div class="container">
        <div class="row  my-5 justify-content-between">
            <div class="col-6">
                <h5>Farm to table</h5>
                <span>Aliquam erat volutpat. Ut quis ligula a magna blandit finibus. Suspendisse maximus lacus non nunc lacinia lobortis.</span>
            </div>
            <div class="col-2">
                <button class="read">READ OUR BLOG <i class="fas fa-book-reader"></i></button>
            </div>
        </div>
        <div class="row">
            <div class="col-8 p-4">
                <div class="row">
                    <div class="col-12">
                        <div class="immagine">
                            <img src="../../assets/img/single-post-img3.jpg">
                            <div class="info text-center">
                                <a href="#">
                                    <div class="link">
                                        <i class="fas fa-link"></i>
                                    </div>
                                    <div class="textlink">
                                        Food Corner: Top Japanese Restaurants for Sushi
                                    </div>
                                </a>
                            </div>
                        </div>
                        <div class="textprincipale">
                            <div class="titolo">
                                <h5>Food Corner: Top Japanese Restaurants for Sushi</h5>
                                <span>By <a href="#">Admin</a> | March 25th, 2020</span>
                            </div>
                            <div class="text">
                                Suspendisse at semper odio. Nam fringilla scelerisque tincidunt. Orci varius natoque penatibus et magnis dis parturient montes, nascetur ridiculus mus. Donec tincidunt posuere ornare. Phasellus placerat odio non feugiat sollicitudin. Integer vitae elementum ex. Sed porttitor, diam eget convallis volutpat, arcu tellus facilisis nulla, id dignissim orci leo id
                            </div>
                            <div>
                                <span>Read More</span>

                            </div>
                        </div>
                    </div>
                    <div class="col-6 p-3" v-for="(element, index) in farm" :key="index">
                        <div class="schede text-center">
                            <Popcard :piatto="element"/>
                            <div class="titolo">{{element.title}}</div>
                            <span>By <a href="#">{{element.author}}</a> | {{element.data}}</span>
                        </div>
                    </div>
                    <div class="col-12 text-center load">
                        <span>LOAD MORE POST</span>
                    </div> 
                </div>
            </div>
                
            <div class="col-4 p-4">
                <div class="row">
                    <div class="col-12 mb-5 text-center latest-recipes">
                        <img src="../../assets/img/ad-bg.jpg" alt="">
                        <h5>VIEW OUR LATEST RECIPES</h5>
                    </div>
                    <div class="col-12 mb-5 singapore">
                        <img src="../../assets/img/singapore-featured-image-600x395.jpg">
                        <div><i class="fas fa-globe-europe"></i> VIEW ALL CITY GUIDES</div>
                        <h5>City Guide: Singapore</h5>
                    </div>
                    <div class="col-12 mb-5">
                        <input class="search" type="text" placeholder="Search..."> 
                        <h5 class="titsocial">Follow US</h5>
                        <div>
                            <a href="#" class="logoSocial me-3">
                                <i class="fa-brands fa-facebook-f"></i>
                                <span class="nomiSocial">Facebook</span>
                            </a>
                            <a href="#" class="logoSocial me-3">
                                <i class="fa-brands fa-instagram"></i>
                                <span class="nomiSocial">Instagram</span>
                            </a>
                            <a href="#" class="logoSocial me-3">
                                <i class="fa-brands fa-twitter"></i>
                                <span class="nomiSocial">Twitter</span>
                            </a>
                            <a href="#" class="logoSocial me-3">
                                <i class="fa-brands fa-youtube"></i>
                                <span class="nomiSocial">Youtube</span>
                            </a>
                            <a href="#" class="logoSocial me-3">
                                <i class="fab fa-pinterest-p"></i>
                                <span class="nomiSocial">Pinterest</span>
                            </a>
                        </div>   
                    </div>
                    <div class="col-12 mb-4">
                        <div class="row poprec">
                            <div class="col-6 popolari text-center">Popular</div>
                            <div class="col-6 recente text-center">Recent</div>
                        </div>
                    </div>
                    <div class="col-12 pop">
                        <img src="../../assets/img/single-post-img3.jpg">
                        <div>
                            <h6>Food Corner: Top Japanese Restaurants for Sushi</h6>
                            <span>March 25th, 2020</span>
                        </div>
                    </div>
                    <div class="col-12 pop">
                        <img src="../../assets/img/singapore-featured-image-600x395.jpg">
                        <div>
                            <h6>City Guide: Singapore</h6>
                            <span>March 25th, 2020</span>
                        </div>
                    </div>
                    <div class="col-12 pop">
                        <img src="../../assets/img/Mixed-fruits-600x395.jpg">
                        <div>
                            <h6>6 Nutrional Tips to Help Burn Body Fat</h6>
                            <span>March 25th, 2020</span>
                        </div>
                    </div>
                    <div class="col-12">
                        <Twitter />
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
import Popcard from '../commons/Popcard.vue'
import farm from '../../assets/data/farm'
import Twitter from '../commons/Twitter.vue'
export default {
  components: { 
      Popcard,
    Twitter,
    },
    name: 'Farm',
    data(){
        return {
            farm: farm,
        }
    }

}
</script>

<style lang="scss" scoped>
@import '../../assets/style/variables.scss';
.pop {
    height: 50px;
    display: flex;
    margin: 10px 0;
    img {
        width: 50px;
        height: 50px;
        object-fit: cover;
        border-radius: 50%;
    }
    div {
        display: inline-block;
        height: 50px;
        margin: 0 0px 0 10px;
        h6 {
            font-weight: bold;
        }
        span {
            color: #afafaf;
        }
    }
}

.poprec {
    border: solid 1px #afafaf;
    border-radius: 3px;
}

.popolari {
    border-right: solid 1px #afafaf;
    background-color: #fff;
    line-height: 50px;
    font-size: 20px;
}
.recente {
    line-height: 50px;
    font-size: 20px;
}

.immagine {
    position: relative;
    a {
        text-decoration: none;
        color: #fff;
    }
}
img {
    width: 100%;
}
.schede {
    background-color: #fff;
    padding-bottom: 20px;
    min-height: 400px;
    .titolo {
        font-weight: bold;
        font-size: 20px;
        padding: 10px 30px;
    }

    span {
      color: #afafaf;
      a {
          text-decoration: none;
          color: #000;
      }
    }
}
.info {
    position: absolute;
    top: 0;
    background: linear-gradient(rgba(255,255,255,.3) ,$mainColor 70%);
    width: 100%;
    height: 100%;
    font-size: 18px;
    color: #fff;
    padding: 80px;
    display: none;

    .link {
        padding: 10px 14px;
        color: $mainColor;
        background: #fff;
        display: inline-block;
        border-radius: 50%;
    }
    
}
.textprincipale {
    padding: 40px;
    font-size: 23px;
    background-color: #fff;

    

    .titolo {
        padding-bottom: 20px;
        border-bottom: dotted 2px #afafaf;
        h5 {
            font-weight: bold;
            font-size: 25px
        }
        span {
            display: inline-block;
            font-size: 15px;
        }
        a {
            text-decoration: none;
            color: #000;
        }
    }
    .text {
        margin: 20px 0;
        color: #6a6a6a;
        font-size: 18px;
        line-height: 30px;
    }

    button {
        text-transform: uppercase;
        font-size: 11px;
        color: #fff;
        background-color: $mainColor;
        border: none;
        border-radius: 2px;
        padding: 9px 20px;
        margin-bottom: 20px;
    }
}
.immagine:hover .info{
    display: block;
}

.load {
   background-color: rgb(229, 229, 218); 
   margin: 20px 5px 100px 5px;
   padding: 15px 0;
   font-weight: bold;
   transition: .5s;
}

.load:hover {
    background-color: #39403e;
    color: #fff;
}

.read {
    background-color: $mainColor;
    color: #fff;
    border: none;
    border-radius: 2px;
    padding: 10px 25px;
}

.latest-recipes {
    position: relative;
    h5 {
        position: absolute;
        top: 50%;
        left: 50%;
        transform: translate(-50%, -50%);
        font-size: 30px;
    }
}
.singapore {
    cursor: pointer;
    position: relative;
    padding-bottom: 50px;
    border-bottom: solid 1px #6a6a6a;
    div {
        background-color: $mainColor;
        color: #fff;
        text-align: center;
        padding: 12px 0;
        transition: 0.4;
    }
    div:hover {
        filter: brightness(0.9);
    }
    h5 {
        background-color: rgba(0, 0, 0, 0.7);
        display: inline-block;
        color: #fff;
        padding: 12px 15px;
        font-size: 25px;
        position: absolute;
        top: 55%;
    }
}

.search {
    width: 100%;
    border: solid 1px #afafaf;
    border-radius: 3px;
    padding: 10px 50px;
}

.titsocial {
    margin: 40px 0;
    color: $mainColor;
    font-size: 20px;
    font-weight: bold;
}
.logoSocial {
    display: inline-block;
    color: #000;
    text-decoration: none;
    height: 40px;
    width: 40px;
    font-size: 15px;
    position: relative;
    text-align: center;
    border: solid 1px #6a6a6a;
    border-radius: 3px;
    padding: 7px;
    background-color: #afafaf;
}

.logoSocial:hover .nomiSocial {
display: block;
}
.nomiSocial {
position: absolute;
top: 40px;
left: 0px;
transform: translateX(-30%);
display: none;
font-size: 15px;
}
</style>