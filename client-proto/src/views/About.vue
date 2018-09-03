<template>
  <div class="about">





<div id="functionBasedDelay">
  <div class="line">
    <div class="small square1 el">
      Hey 
    </div>
  </div>
  <div class="line">
    <div class="small square1 el">
      There!
     </div>
  </div>
</div>


  <div id="duration">
  <div class="square el fade-in one">
Heya,I’m Fahri,a software <br> developer from Jakarta.<br> Please take a look around!     
  </div>
</div>
     

<div id="duration-summary">
  <div class="square-summary el-s fade-in one-s ">

<p>I am passionate about building excellent software that improves the lives of those around me. I specialize in creating software for clients ranging from individuals and small-businesses all the way to <br>large enterprise corporations.All of my work is produced locally from Moscow, Idaho. <br>
What would you do if you had a software expert available at your fingertips?.</p>

  </div>
</div>

  </div>

</template>


<script>
import anime from "animejs";

// import { mydiv } from "../assets/anime.js/animate.js";

export default {
  data() {
    return {
      data: {
        show: false
      }
    };
  },
  methods: {
    functionBasedDelay() {
      anime({
        targets: "#functionBasedDelay .el",
        translateY: 220,
        direction: "alternate",
        loop: false,
        delay: function(el, i, l) {
          return i * 600;
        }
      });
    },

    mySummary() {
      anime({
        targets: "#duration-summary .el-s",
        translateY: -155,
        duration: 5000
      });
    },

    myDescription() {
      anime({
        targets: "#duration .el",
        translateX: 180,
        duration: 5000
      });
    }
  },

  mounted() {
    let self = this;
    setTimeout(function() {
      self.functionBasedDelay();
    }, 600);

    setTimeout(function() {
      self.mySummary();
    }, 6000);

    setTimeout(function() {
      self.myDescription();
    }, 3600);
  }
};
</script>

<style scoped>
@-webkit-keyframes fadeIn {
  from {
    opacity: 0;
  }
  to {
    opacity: 1;
  }
}
@-moz-keyframes fadeIn {
  from {
    opacity: 0;
  }
  to {
    opacity: 1;
  }
}
@keyframes fadeIn {
  from {
    opacity: 0;
  }
  to {
    opacity: 1;
  }
}

.fade-in {
  opacity: 0; /* make things invisible upon start */
  -webkit-animation: fadeIn 1s ease-in 0s 1 normal forwards; /* call our keyframe named fadeIn, use animattion ease-in and repeat it only 1 time */
  -moz-animation: fadeIn 1s ease-in 0s 1 normal forwards;
  animation: fadeIn 1s ease-in 0s 1 normal forwards;
}

.fade-in.one {
  -webkit-animation-delay: 0.7s;
  -moz-animation-delay: 0.7s;
  animation-delay: 3.5s;
}
.fade-in.one-s {
  -webkit-animation-delay: 0.7s;
  -moz-animation-delay: 0.7s;
  animation-delay: 6s;
}

.fade-enter-active,
.fade-leave-active {
  transition: opacity 0.5s;
}
.fade-enter, .fade-leave-to /* .fade-leave-active below version 2.1.8 */ {
  opacity: 0;
}
.small {
  margin: 3px;
  width: 200px;
  height: 200px;
  -webkit-animation: fadein 4s linear forwards;
  /* animation: fadeinout 4s linear forwards; */
}

@-webkit-keyframes fadein {
  0%,
  100% {
    opacity: 0;
  }
  50% {
    opacity: 1;
  }
}

#functionBasedDelay {
  display: flex;
  /* border: blue solid 2px; */
  /* bor */
  /* border: red solid 2px; */
  justify-content: center;
  /* text-align: center; */
  /* flex-wrap: wrap; */
}
.small {
  /* border: blue solid 2px; */
  color: white;
  font-size: 150px;
  /* min-width: 400px; */
}
.square1 {
  /* margin: 500px; */
  color: white;
  margin: 20px;
  /* border: purple solid 2px; */

  /* border: blue solid 2px; */
  /* width: 660px; */
  /* font-size: 40px; */
}
.square {
  color: white;
  /* border: yellow solid 2px; */
  width: 450px;
  font-size: 36px;
  font-weight: bold;
  text-align: right;
}

#duration {
  /* margin-left: 0px; */
  text-align: left;
  width: 44%;
  /* border: blue solid 2px; */
}

.square-summary {
  font-weight: 600;
  float: right;
  color: white;
  margin-right: 70px;
  /* border: green solid 2px; */
  text-align: left;
  width: 47%;
  left: 80px;
}
</style>
