<template>
  <div id="container">
    <div class="dot"></div>
    <div class="pulse"></div>
  </div>
</template>

<script>
export default {}
</script>

<style scoped>
#container {
  position: relative;
  background: #40453f;
}

.pulse {
  width: 10px;
  height: 10px;
  border: 5px solid #01ff4d;
  -webkit-border-radius: 30px;
  -moz-border-radius: 30px;
  border-radius: 30px;
  background-color: #427146;
  z-index: 99;
  position: absolute;
  top: -5px;
  left: -5px;
}

.dot {
  border: 10px solid #01ff4d;
  background: transparent;
  -webkit-border-radius: 60px;
  -moz-border-radius: 60px;
  border-radius: 60px;
  height: 50px;
  width: 50px;
  -webkit-animation: pulse 3s ease-out;
  -moz-animation: pulse 3s ease-out;
  animation: pulse 3s ease-out;
  -webkit-animation-iteration-count: infinite;
  -moz-animation-iteration-count: infinite;
  animation-iteration-count: infinite;
  position: absolute;
  top: -25px;
  left: -25px;
  z-index: 99;
  opacity: 0;
}

/* @keyframes pulse {
 0% {
    -moz-transform: scale(0);
    opacity: 0.0;
 }
 25% {
    -moz-transform: scale(0);
    opacity: 0.1;
 }
 50% {
    -moz-transform: scale(0.1);
    opacity: 0.3;
 }
 75% {
    -moz-transform: scale(0.5);
    opacity: 0.5;
 }
 100% {
    -moz-transform: scale(1);
    opacity: 0.0;
 }
} */

@keyframes pulse {
  0% {
    -webkit-transform: scale(0);
    opacity: 0;
  }
  25% {
    -webkit-transform: scale(0);
    opacity: 0.1;
  }
  50% {
    -webkit-transform: scale(0.1);
    opacity: 0.3;
  }
  75% {
    -webkit-transform: scale(0.5);
    opacity: 0.5;
  }
  100% {
    -webkit-transform: scale(1);
    opacity: 0;
  }
}
@media screen and (max-width: 850px) {
  .pulse {
    width: 6px;
    height: 6px;
    border: 3px solid #01ff4d;
    top: -2.5px;
    left: -3px;
  }
  .dot {
    border: 6px solid #01ff4d;
    background: transparent;
    height: 30px;
    width: 30px;
    top: -15px;
    left: -15px;
  }
}
@media screen and (max-width: 670px) {
  .pulse {
    top: -3px;
    left: -2.5px;
  }
}
@media screen and (max-width: 450px) {
  .pulse {
    top: -3px;
    left: -3.5px;
  }
}
</style>
