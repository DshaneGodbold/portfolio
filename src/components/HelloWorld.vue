<template>
  <div class="main">
    <div class="area">
      <ul class="circles">
        <li></li>
        <li></li>
        <li></li>
        <li></li>
        <li></li>
        <li></li>
        <li></li>
        <li></li>
        <li></li>
        <li></li>
      </ul>
      <img
        class="shane-profile-pic fade-in-fwd"
        alt=""
        src="@/assets/portfolio-pic.jpg"
      />
      <h1>Welcome to D'Shane's Portfolio!</h1>
      <p class="text-focus-in">
        Welcome to my <b>Domain!</b> Check me out I hope you like it~~ ❤️
      </p>
      <h3 class="Google text-focus-in">Google</h3>
      <ul class="pulsate-bck">
        <li>
                    <box-icon type="logo" name="gmail" animation="tada" color='red' />
          <a
            href="https://Dshanegodbold@gmail.com"
            target="_blank"
            rel="noopener"
            >Gmail</a
            >
        </li>
      </ul>
      <h3 class="text-focus-in">Github</h3>
      <ul class="pulsate-bck">
        <li>
          <box-icon type="logo" name="github" animation="spin" color='purple'/>
          <a
            href="https://github.com/DshaneGodbold"
            target="_blank"
            rel="noopener"
            >D'Shane's Github</a>
        </li>
      </ul>
      <h3 class="text-focus-in">Resume</h3>
      <ul class="pulsate-bck">
        <li>
          <box-icon name='file-pdf' type='solid' animation="fade-down" color='orange' />
          <a href="/files/Dshane's SnapIT Resume.pdf" download="">Resume</a>
        </li>
      </ul>
    </div>
  </div>
</template>

<script>
import boxicons from "boxicons";
export default {
  name: "HelloWorld",
  props: {
    msg: String,
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
.shane-profile-pic {
  width: 350px;
  height: auto;
  border-radius: 20px;
}

.fade-in-fwd {
  animation: fade-in-fwd 1.5s cubic-bezier(0.39, 0.575, 0.565, 1) both;
}
@keyframes fade-in-fwd {
  0% {
    transform: translateZ(-80px);
    opacity: 0;
  }
  100% {
    transform: translateZ(0);
    opacity: 1;
  }
}

h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}

.text-focus-in {
  animation: text-focus-in 1.5s cubic-bezier(0.55, 0.085, 0.68, 0.53) both;
}
@keyframes text-focus-in {
  0% {
    filter: blur(12px);
    opacity: 0;
  }
  100% {
    filter: blur(0);
    opacity: 1;
  }
}

.pulsate-bck {
  animation: pulsate-bck 0.5s ease-in-out infinite both;
}


@keyframes pulsate-bck {
  0% {
    transform: scale(1);
  }
  50% {
    transform: scale(0.9);
  }
  100% {
    transform: scale(1);
  }
}

@import url("https://fonts.googleapis.com/css?family=Exo:400,700");

* {
  margin: 0px;
  padding: 0px;
}

body {
  font-family: "Exo", sans-serif;
}

.context {
  width: 100%;
  position: absolute;
  top: 50vh;
}

.context h1 {
  text-align: center;
  color: #fff;
  font-size: 50px;
}

.area {
  background: #2481ac;
  background: -webkit-linear-gradient(to left, #8f94fb, #4e54c8);
  width: 100%;
  height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  flex-direction: column;
}

.circles {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  overflow: hidden;
  pointer-events: none;
}

.circles li {
  position: absolute;
  display: block;
  list-style: none;
  width: 20px;
  height: 20px;
  background: #3fa94e;
  animation: animate 25s linear infinite;
  bottom: -150px;
}

.circles li:nth-child(1) {
  left: 25%;
  width: 80px;
  height: 80px;
  animation-delay: 0s;
}

.circles li:nth-child(2) {
  left: 10%;
  width: 20px;
  height: 20px;
  animation-delay: 2s;
  animation-duration: 12s;
}

.circles li:nth-child(3) {
  left: 70%;
  width: 20px;
  height: 20px;
  animation-delay: 4s;
}

.circles li:nth-child(4) {
  left: 40%;
  width: 60px;
  height: 60px;
  animation-delay: 0s;
  animation-duration: 18s;
}

.circles li:nth-child(5) {
  left: 65%;
  width: 20px;
  height: 20px;
  animation-delay: 0s;
}

.circles li:nth-child(6) {
  left: 75%;
  width: 110px;
  height: 110px;
  animation-delay: 3s;
}

.circles li:nth-child(7) {
  left: 35%;
  width: 150px;
  height: 150px;
  animation-delay: 7s;
}

.circles li:nth-child(8) {
  left: 50%;
  width: 25px;
  height: 25px;
  animation-delay: 15s;
  animation-duration: 45s;
}

.circles li:nth-child(9) {
  left: 20%;
  width: 15px;
  height: 15px;
  animation-delay: 2s;
  animation-duration: 35s;
}

.circles li:nth-child(10) {
  left: 85%;
  width: 150px;
  height: 150px;
  animation-delay: 0s;
  animation-duration: 11s;
}

@keyframes animate {
  0% {
    transform: translateY(0) rotate(0deg);
    opacity: 1;
    border-radius: 0;
  }
  
  100% {
    transform: translateY(-1000px) rotate(720deg);
    opacity: 0;
    border-radius: 50%;
  }
}
</style>