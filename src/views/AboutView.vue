<template>
  <div class="box">
    <div class="lamp">
      <div class="lampLine"></div>
      <div class="lampshade"></div>
      <div class="bulb"></div>
      <div class="ary"></div>
    </div>
    <div class="text">
      <h2>404</h2>
      <p>哦豁,页面不存在!</p>
    </div>
  </div>
</template>

<style>
* {
  padding: 0;
  margin: 0;
}
.box {
  height: 100vh;
  width: 100vw;
  background-color: #000;
  margin: 0 auto;
  overflow: hidden;
}

.box::after {
  content: ' ';
  position: absolute;
  width: 3px;
  height: 3px;
  border-radius: 50%;
  background: transparent;
  box-shadow: 571px 173px #00bcd4, 1732px 143px #00bcd4, 1745px 454px #ff5722, 234px 784px #00bcd4,
    1793px 1123px #ff9800, 1076px 504px #03a9f4, 633px 601px #ff5722, 350px 630px #ffeb3b,
    1164px 782px #00bcd4, 76px 690px #3f51b5, 1825px 701px #cddc39, 1646px 578px #ffeb3b,
    544px 293px #2196f3, 445px 1061px #673ab7, 928px 47px #00bcd4, 168px 1410px #8bc34a,
    777px 782px #9c27b0, 1235px 1941px #9c27b0, 104px 1690px #8bc34a, 1167px 1338px #e91e63,
    345px 1652px #009688, 1682px 1196px #f44336, 1995px 494px #8bc34a, 428px 798px #ff5722,
    340px 1623px #f44336, 605px 349px #9c27b0, 1339px 1344px #673ab7, 1102px 1745px #3f51b5,
    1592px 1676px #2196f3, 419px 1024px #ff9800, 630px 1033px #4caf50, 1995px 1644px #00bcd4,
    1092px 712px #9c27b0, 1355px 606px #f44336, 622px 1881px #cddc39, 1481px 621px #9e9e9e,
    19px 1348px #8bc34a, 864px 1780px #e91e63, 442px 1136px #2196f3, 67px 712px #ff5722,
    89px 1406px #f44336, 275px 321px #009688, 592px 630px #e91e63, 1012px 1690px #9c27b0,
    1749px 23px #673ab7, 94px 1542px #ffeb3b, 1201px 1657px #3f51b5, 1505px 692px #2196f3,
    1799px 601px #03a9f4, 656px 811px #00bcd4, 701px 597px #00bcd4, 1202px 46px #ff5722,
    890px 569px #ff5722, 1613px 813px #2196f3, 223px 252px #ff9800, 983px 1093px #f44336,
    726px 1029px #ffc107, 1764px 778px #cddc39, 622px 1643px #f44336, 174px 1559px #673ab7,
    212px 517px #00bcd4, 340px 505px #fff, 1700px 39px #fff, 1768px 516px #f44336,
    849px 391px #ff9800, 228px 1824px #fff, 1119px 1680px #ffc107, 812px 1480px #3f51b5,
    1438px 1585px #cddc39, 137px 1397px #fff, 1080px 456px #673ab7, 1208px 1437px #03a9f4,
    857px 281px #f44336, 1254px 1306px #cddc39, 987px 990px #4caf50, 1655px 911px #00bcd4,
    1102px 1216px #ff5722, 1807px 1044px #fff, 660px 435px #03a9f4, 299px 678px #4caf50,
    1193px 115px #ff9800, 918px 290px #cddc39, 1447px 1422px #ffeb3b, 91px 1273px #9c27b0,
    108px 223px #ffeb3b, 146px 754px #00bcd4, 461px 1446px #ff5722, 1004px 391px #673ab7,
    1529px 516px #f44336, 1206px 845px #cddc39, 347px 583px #009688, 1102px 1332px #f44336,
    709px 1756px #00bcd4, 1972px 248px #fff, 1669px 1344px #ff5722, 1132px 406px #f44336,
    320px 1076px #cddc39, 126px 943px #ffeb3b, 263px 604px #ff5722, 1546px 692px #f44336;
  animation: animStar 150s linear infinite;
}

@keyframes animStar {
  0% {
    transform: translateY(-10px);
  }

  50% {
    transform: translateY(-1000px);
  }

  100% {
    transform: translateY(-10px);
  }
}

.lamp {
  position: relative;
  margin: 0 auto;
  animation: lamp 4s infinite ease-in-out;
  transform-origin: top;
  transform: rotateZ(300deg);
}

@keyframes lamp {
  0% {
    transform: rotateZ(300deg);
  }

  50% {
    transform: rotateZ(420deg);
  }

  100% {
    transform: rotateZ(300deg);
  }
}

.lampLine {
  /* 灯线 */
  content: '';
  position: absolute;
  top: 0;
  left: 50%;
  transform: translateX(-50%);
  width: 5px;
  height: 120px;
  background-image: linear-gradient(#795548, #00bcd4);
}

.lampshade {
  /* 灯罩 */
  position: absolute;
  left: 50%;
  top: 120px;
  transform: translateX(-50%);
  width: 100px;
  height: 45px;
  background-color: #aaffff;
  border-top-left-radius: 50%;
  border-top-right-radius: 50%;
  z-index: 9;
  box-shadow: 0 0 15px #aaffff;
}

.lampshade::before {
  content: '';
  position: absolute;
  bottom: -4px;
  width: 100%;
  height: 10px;
  background-color: #bdfcff85;
  border-radius: 50%;
}

.bulb {
  position: absolute;
  left: 50%;
  top: 148px;
  transform: translateX(-50%);
  background-color: #fff;
  width: 35px;
  height: 33px;
  border-radius: 50%;
  box-shadow: 0 0 8px 8px #c1c1c1, 0 0 16px 16px #c1c1c1, 0px 0px 32px 20px #c1c1c1;
}

.ary {
  position: absolute;
  left: 50%;
  transform: translateX(-50%);
  width: 100px;
  opacity: 0.5;
  top: 165px;
  border-right: 150px solid transparent;
  border-bottom: 2000px solid #55aaff;
  border-left: 150px solid transparent;
  filter: blur(5px);
}

.ary::before {
  position: absolute;
  content: '';
  left: 50%;
  transform: translateX(-50%);
  width: 120px;
  opacity: 0.5;
  border-right: 120px solid transparent;
  border-bottom: 2000px solid linear-gradient(#795548, #00bcd4);
  border-left: 120px solid transparent;
}

.text {
  position: absolute;
  width: 100%;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  text-align: center;
}

.text h2 {
  font-size: 100px;
}

.text p {
  font-size: 75px;
}
</style>
