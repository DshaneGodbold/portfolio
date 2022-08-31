<template>
<!--Hey! This is the original version
of Simple CSS Waves-->

<div class="header">
<!--Content before waves-->
<div class="inner-header flex">
<!--Just the logo.. Don't mind this-->
<path fill="#FFFFFF" stroke="#000000" stroke-width="10" stroke-miterlimit="10" d="M57,283" />
<h1 id="letter-bounce" value="letter-bounce" class="letter-bounce">About Me</h1>
<p>Hello <box-icon name="hand" type="solid" color="#ffffff" animation="tada"/> !
 My name is Dshane Godbold, <box-icon name='happy-beaming' type='solid' animation='spin' color='#ffffff'/>
and I am a computer programming Apprentice at SnapIT Solutions!<box-icon name='business' type='solid' animation='flashing' color='#03ff00'/>
 I am working on this portoflio
 to show off my skills so I think this would be a good way to show it off! <box-icon name='heart' type='solid' color='#ff0000'/> </p>
</div>

<div class="pics">

  <img
  class="china-pic"
  alt=""
  src="@/assets/china.jpg"
  />
  <img
  class="spectrum-pic"
  alt=""
  src="@/assets/spectrum.jpg"
  />
  <img
  class="happy-pic"
  alt=""
  src="@/assets/happy.jpg"
  />
</div>
  




<div>


  
</div>

<!--Waves Container-->
<div>
<svg class="waves" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink"
viewBox="0 24 150 28" preserveAspectRatio="none" shape-rendering="auto">
<defs>
<path id="gentle-wave" d="M-160 44c30 0 58-18 88-18s 58 18 88 18 58-18 88-18 58 18 88 18 v44h-352z" />
</defs>
<g class="parallax">
<use xlink:href="#gentle-wave" x="48" y="0" fill="rgba(255,255,255,0.7" />
<use xlink:href="#gentle-wave" x="48" y="3" fill="rgba(255,255,255,0.5)" />
<use xlink:href="#gentle-wave" x="48" y="5" fill="rgba(255,255,255,0.3)" />
<use xlink:href="#gentle-wave" x="48" y="7" fill="#fff" />
</g>
</svg>
</div>
<!--Waves end-->

</div>
<!--Header ends-->

<!--Content starts-->
<!--Content ends-->
</template>

<script>
export default {
  name: "MySkillsBackground",
  props: {
    msg: String,
  },
};



</script>

<style>


@import url(//fonts.googleapis.com/css?family=Lato:300:400);

body {
  margin:0;
}

.pics{
  padding: 15px;
  text-align: center;
}

.spectrum-pic{
  object-fit: cover;
  width: 350px;
  height:279px;
}

.china-pic{
  object-fit: cover;
  width: 350px;
  height:279px;
}

.happy-pic{
  object-fit: cover;
  width: 350px;
  height:279px;
}


p  {
    font-family: 'Baloo Thambi', cursive;
    font-weight: 300;
    font-size: xx-large;
    text-align: inherit;
    padding-bottom: 10cm;
    animation: glow 8s ease-in-out 2s infinite;
}

@keyframes glow{
  0%, 100%{
    color: #fff;
    text-shadow: 0 0 10px #8a2be2, 0 0 50px #8a2be2, 0 0 100px #8a2be2;
  }

  10%, 90%{
    color: #fff;
    text-shadow: none;
  }
}

h1 {
  font-family: 'Lato', sans-serif;
  font-weight:300;
  letter-spacing: 2px;
  font-size:52px;
}

.letter-bounce
{
  opacity: 0;
  transform: translateY(-5rem);
  animation: bounce 5000ms ease-in-out infinite;
  animation-delay: var(--delay);
}

@keyframes bounce
{
  0%, 100%
  {
    transform: translateY(-5rem);
    opacity: 0;
  }
  10%
  {
    transform: translateY(0) scaleY(0.8) scaleX(1.2);
    opacity: 1;
  }
  20%
  {
    transform: translateY(-2.5rem) scaleY(1) scaleX(1);
  }
  30%
  {
    transform: translateY(0) scaleY(1);
    opacity: 1;
  }
  90%
  {
    transform: translateY(0) scaleY(1);
    opacity: 1;
  }
  95%
  {
    opacity: 0;
  }
}




.header {
  position:relative;
  text-align:center;
  background: linear-gradient(60deg, rgba(84,58,183,1) 0%, rgba(0,172,193,1) 100%);
  color:white;
}

.inner-header {
  height:65vh;
  width:100%;
  margin: 0;
  padding: 0;
}


.waves {
  position:relative;
  width: 100%;
  height:15vh;
  margin-bottom:-7px; /*Fix for safari gap*/
  min-height:100px;
  max-height:150px;
}

.content {
  position:relative;
  height:20vh;
  text-align:center;
  background-color: white;
}

/* Animation */

.parallax > use {
  animation: move-forever 25s cubic-bezier(.55,.5,.45,.5)     infinite;
}
.parallax > use:nth-child(1) {
  animation-delay: -2s;
  animation-duration: 7s;
}
.parallax > use:nth-child(2) {
  animation-delay: -3s;
  animation-duration: 10s;
}
.parallax > use:nth-child(3) {
  animation-delay: -4s;
  animation-duration: 13s;
}
.parallax > use:nth-child(4) {
  animation-delay: -5s;
  animation-duration: 20s;
}
@keyframes move-forever {
  0% {
   transform: translate3d(-90px,0,0);
  }
  100% { 
    transform: translate3d(85px,0,0);
  }
}
/*Shrinking for mobile*/
@media (max-width: 768px) {
  .waves {
    height:40px;
    min-height:40px;
  }
  .content {
    height:30vh;
  }
  h1 {
    font-size:24px;
  }
}
</style>
