<template>
  <div id="homeContent">
    <!-- image section start  -->
    <div class="d-md-block d-none">
      <div class="image firstImage row">
        <div class="boxA1">
          <h2 class="makeForYou">MAKE FOR YOU</h2>
          <h2 class="pistons">PISTONS</h2>
        </div>
        <div class="boxA2">
          <div class="a2Text">
            <h2>YOU WERE MADE TO</h2>
            <h2>MAKE AN IMPACT.</h2>
          </div>
          <button class="shopBtn">SHOP PENS</button>
        </div>
      </div>
      <div class="image row">
        <div class="boxB1">
          <div class="b1Text">
            <h2>MAKE FOR THE BEST</h2>
            <h2>CHANGE MAKERS.</h2>
          </div>
          <button class="b1shopBtn">SHOP PENS</button>
        </div>
        <div class="boxB2"></div>
      </div>
      <div class="image row">
        <div class="boxC1"></div>
        <div class="boxC2">
          <div class="a2Text">
            <h2>SAVOUR THE PRESENT.</h2>
          </div>
          <button class="shopBtn">SHOP PENS</button>
        </div>
      </div>
      <div class="image row">
        <div class="boxD">
          <div>
            <img
              src="../assets/image/ervan-m-wirawan-KY2baho4jnA-unsplash 1.png"
            />
          </div>
          <div>
            <div class="lastText">WHERE QUALITY MEETS CLASS.</div>
            <h2 class="lastMakeForYou">MAKE FOR YOU</h2>
            <h2 class="pistons">PISTONS</h2>
            <button class="dshopBtn">SHOP THE FALL 2023 COLLECTION</button>
          </div>
        </div>
      </div>
    </div>
    <!-- image section for laptop screen  end -->
    <!-- image section for mobile screen start  -->
    <div class="d-md-none d-block">
      <div class="image firstImage row">
        <div class="boxA1">
          <h2 class="makeForYou">MAKE FOR YOU</h2>
          <h2 class="pistons">PISTONS</h2>
        </div>
      </div>
      <div class="image row">
        <div class="boxA2">
          <div class="a2Text">
            <h2>YOU WERE MADE TO</h2>
            <h2>MAKE AN IMPACT.</h2>
          </div>
          <button class="shopBtn">SHOP PENS</button>
        </div>
      </div>
      <div class="image row">
        <div class="boxB1">
          <div class="b1Text">
            <h2>MAKE FOR THE BEST</h2>
            <h2>CHANGE MAKERS.</h2>
          </div>
          <button class="b1shopBtn">SHOP PENS</button>
        </div>
      </div>
      <div class="image row">
        <div class="boxB2"></div>
      </div>
      <div class="image row">
        <div class="boxC1"></div>
      </div>
      <div class="image row">
        <div class="boxC2">
          <div class="a2Text">
            <h2>SAVOUR THE PRESENT.</h2>
          </div>
          <button class="shopBtn">SHOP PENS</button>
        </div>
      </div>
      <div class="image row">
        <div class="boxD">
          <div>
            <img
              src="../assets/image/ervan-m-wirawan-KY2baho4jnA-unsplash 1.png"
            />
          </div>
          <div>
            <div class="lastText">WHERE QUALITY MEETS CLASS.</div>
            <h2 class="lastMakeForYou">MAKE FOR YOU</h2>
            <h2 class="pistons">PISTONS</h2>
            <button class="dshopBtn">SHOP THE FALL 2023 COLLECTION</button>
          </div>
        </div>
      </div>
    </div>

    <button class="feedback">FEEDBACK</button>

    <div class="noSticky">
      <!-- about section for laptop start  -->
      <div class="about row" id="about">
        <div class="aboutPic">
          <div class="imageCarousal">
            <img src="../assets/image/carousel_img_1.png" class="pic" />
            <img src="../assets/image/carousel_img_2.png" class="pic" />
            <img src="../assets/image/carousel_img_3.png" class="pic" />
            <img src="../assets/image/carousel_img_4.png" class="pic" />
          </div>
        </div>
        <div class="aboutPistons">
          <h1>ABOUT PISTONS</h1>
          <p>
            Established in 1897, our beloved fountain pen haven, 'PISTONS,' has
            been a haven for pen enthusiasts for generations. With a
            century-long dedication to fine writing instruments, we've bridged
            tradition and modernity, offering a curated selection of vintage and
            contemporary fountain pens. Our little shop, nestled in the heart of
            town, continues to inspire a love for the art of writing, connecting
            past and present through the timeless elegance of ink on paper
          </p>
        </div>
      </div>
      <!-- about section  for laptop end  -->

      <!-- testimonials section start  -->
      <!-- <hr> -->
      <div class="testimonials">
        <h1 class="testimonialsHeading">TESTIMONIALS</h1>
        <div class="container">
          <TestimonialCard
            v-for="item in testimonialsData"
            :key="item.image"
            :img="item.image"
            :name="item.name"
            :message="item.message"
          />
        </div>
      </div>
    </div>
    <!-- testimonials section end  -->
  </div>
</template>
<script>
import axios from "axios";
import TestimonialCard from "./TestimonialCard.vue";
export default {
  name: "HomePage",
  components: { TestimonialCard },
  data() {
    return {
      testimonialsData: [
        {
          name: "Alex P.",
          message:
            "I stumbled upon this shop, and their selection blew me away. The user-friendly website made my shopping experience a breeze!",
          image: "https://i.ibb.co/vmYY6tY/img1.png",
        },
        {
          name: "Emily S.",
          message:
            "The checkout process was seamless, and the responsive design worked flawlessly on my mobile device. I'll definitely be coming back!",
          image: "https://i.ibb.co/k29V4KN/img2.png",
        },
        {
          name: "David R.",
          message:
            "Their site's intuitive navigation made finding the perfect pen a joy. Five stars for both their products and web design!",
          image: "https://i.ibb.co/Mcz1SWT/img3.png",
        },
        {
          name: "Lisa M.",
          message:
            "I appreciate the attention to detail in both their pens and website. A visually stunning and user-focused online shop.",
          image: "https://i.ibb.co/94fW8xZ/img4.png",
        },
      ],
    };
  },
  created() {
    // this.fetchData();
  },
  methods: {
    async fetchData() {
      try {
        const res = await axios(
          "https://elitefit4you.com/test-api/testimonials.json"
        );
        this.testimonialsData = res.data.testimonials;
        console.log("this.testimonialsData:", this.testimonialsData);
      } catch (error) {
        console.log("error:", error);
      }
    },
  },
};
</script>
<style>
#homeContent {
  margin-top: 20vh;
  width: 100vw;
  box-sizing: border-box;
}
.image {
  width: 100vw;
  max-height: 100vh;
  position: sticky;
  top: 20vh;
  z-index: -10;
}
.firstImage {
  margin-top: 15vh;
}
.boxA1 {
  width: 50vw;
  background-image: url("../assets/image/pexels-energepiccom-110473\ 1.png");
  height: 93vh;
  background-size: cover;
  background-repeat: no-repeat;
}
.boxA2 {
  width: 50vw;
  background-image: url("../assets/image/pexels-pixabay-261450\ 1.png");
  height: 93vh;
  background-size: cover;
  background-repeat: no-repeat;
}

.boxB1 {
  width: 50vw;
  background-image: url("../assets/image/pexels-janson-a-753695 1.png");
  height: 93vh;
  background-size: cover;
  background-repeat: no-repeat;
}
.boxB2 {
  width: 50vw;
  background-image: url("../assets/image/pexels-anete-lusina-5240857 1.png");
  height: 93vh;
  background-size: cover;
  background-repeat: no-repeat;
}

.boxC1 {
  width: 50vw;
  background-image: url("../assets/image/Frame 12.png");
  height: 93vh;
  background-size: cover;
  background-repeat: no-repeat;
}
.boxC2 {
  width: 50vw;
  background-image: url("../assets/image/omar-al-ghosson-zhQ6WmcrahQ-unsplash 1.png");
  height: 93vh;
  background-size: cover;
  background-repeat: no-repeat;
}

.boxD {
  height: 93vh;
  position: relative;
}
.boxD img {
  width: 100vw;
  height: 93vh;
}
.boxD > :nth-child(2) {
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  text-align: center;
}
.boxD > :nth-child(2) > button {
  margin: auto;
}
.feedback {
  transform: rotate(-90deg);
  position: fixed;
  top: 50%;
  right: -30px;
  transform-origin: center center;
}

.about {
  width: 100vw;
  height: 93vh;
  background-color: white;
}
.noSticky {
  z-index: 10;
}
.aboutPic {
  display: flex;
  justify-content: center;
  align-items: center;
  width: 50vw;
  height: 93vh;
}
.imageCarousal {
  display: flex;
  width: 40vw;
  overflow-x: scroll;
}
.imageCarousal img {
  width: 100%;
}
.aboutPistons {
  display: flex;
  justify-content: center;
  flex-direction: column;
  padding: 10%;
  width: 50vw;
  height: 93vh;
}

.pic {
  width: 40vw;
  height: 70vh;
}
.testimonials {
  width: 100vw;
  background-color: white;
  padding-bottom: 50px;
}
.testimonials > .testimonialsHeading {
  text-align: center;
  font-weight: 700;
  font-size: 36px;
  line-height: 45.46px;
}
.container {
  width: 90vw;
  padding-top: 70px;
  margin: auto;
  display: flex;
  justify-content: space-around;
}

.makeForYou {
  color: white;
  text-align: center;
  margin-top: 60%;
}
.pistons {
  color: white;
  text-align: center;
  margin-top: 30px;
  font-family: "pridi";
}
.a2Text {
  color: white;
  text-align: center;
  margin-top: 60%;
  font-size: x-large;
  font-family: -webkit-body;
}
.shopBtn {
  align-items: center;
  border-radius: 20px;
  height: 35px;
  width: 180px;
  font-weight: 700;
  border: 4px solid #ffecc1;
  margin-left: 38%;
  margin-top: 15px;
}
.b1Text {
  color: black;
  text-align: center;
  margin-top: 60%;
  font-size: x-large;
  font-family: -webkit-body;
}
.b1shopBtn {
  align-items: center;
  border-radius: 20px;
  height: 35px;
  width: 180px;
  font-weight: 700;
  background-color: black;
  color: white;
  border: 4px solid #ffecc1;
  margin-left: 38%;
  margin-top: 15px;
}
.lastText {
  color: white;
  text-align: center;
  margin-top: 10%;
  font-size: xxx-large;
  font-weight: 300;
}
.lastMakeForYou {
  color: white;
  text-align: center;
  margin-top: 60px;
}
.dshopBtn {
  align-items: center;
  border-radius: 20px;
  height: 45px;
  width: 360px;
  font-weight: 700;
  border: 4px solid #ffecc1;
  margin-left: 38%;
  margin-top: 60px;
}
@media only screen and (max-width: 815px) {
  #about {
    display: flex;
    height: auto;
  }
  .imageCarousal {
    width: 80vw;
    overflow-x: scroll;
  }
  #about > div {
    width: 100%;
  }
}
@media only screen and (max-width: 767px) {
  .container {
    width: 100vw;
    flex-direction: column;
  }
  .item {
    margin: 10px;

    img {
      margin: 50px 0px;
    }
  }
  .boxA1 {
    width: 100vw;
  }
  .boxA2 {
    width: 100vw;
  }
  .boxB1 {
    width: 100vw;
  }
  .boxB2 {
    width: 100vw;
  }
  .boxC1 {
    width: 100vw;
  }
  .boxC2 {
    width: 100vw;
  }

  .boxD img {
    width: 100vw;
    height: 93vh;
  }
  .boxD > :nth-child(2) {
    position: static;
    background-color: black;
  }
  .boxD {
    height: 93vh;
    display: flex;
    flex-direction: column;
    align-items: center;
    background-color: black;
  }
  .boxD img {
    width: 100vw;
    height: auto;
  }
  .boxD > :nth-child(1) {
  }
  .boxD > :nth-child(2) {
    width: 100vw;
    position: static;
    transform: translate(0%, 0%);
  }
  .boxD > :nth-child(2) > button {
    margin: auto;
    width: 80vw;
  }
  .boxD > :nth-child(2) > div {
    font-size: 24px;
  }
}
</style>
