<template>

<Head>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=DotGothic16&display=swap" rel="stylesheet">
</Head>


  <v-app>


    <v-app-bar color="#111">
      <v-container>
        <v-layout>


    <div class="text-h6 text-white">
      <b>kooke</b>
    </div>
    <div class="text-h4 text-white">
      <b>Lab</b>
    </div>

    <v-divider></v-divider>

    <div>
      <b>about</b>
    </div>

        </v-layout>
      </v-container>
    </v-app-bar>













  <div class="main-component">





    <v-row>
      <v-col class="d-flex">


        <div class="box">
          <img class="lab" src="@/assets/image/lab.png">

          <p class="skill">
            ▼ SKILL
          </p>

          <p class="work">
            ▼ WORK
          </p>

          <p class="sns">
            ▼ SNS
          </p>

          <p class="github">
            ▼ GitHub
          </p>

          <p class="exit">
            ▼ EXIT
          </p>

        </div>


              <!-- <img class="lab" src="@/assets/image/lab.png">
                <p class="top-left">左上テキスト</p>
                <p class="top-right">右上テキスト</p>
                <p class="bottom-left">左下テキスト</p>
                <p class="bottom-right">右下テキスト</p>
                <p class="center">天地中央テキスト</p> -->
      </v-col>
    </v-row>
    <div class="text-h6 text-white float-right">
      <b>ver.0.0.1</b>
    </div>
  </div>
    
  </v-app>
</template>

<style>
.v-application{
  font-family: 'DotGothic16', sans-serif;
}


  .main-component {
    margin: 0 auto 0 auto;
    padding: 60px 5% 5% 5%;
    background-color: #111;
  }

  .lab {
    width: 90%;
    margin: 0 auto 0 auto;
    margin-top: 20px;
    margin-bottom: 20px;
  }

  



  .box img{
  width: 100%;
  height: auto;
}
p{
  margin: 0;
  padding: 0;
  color: #FFF;
  font-size: 32px;
}

.box{
  position: relative;
}
.skill {
  position: absolute;
  top: 28%;
  left: 11%;
  font-size: 20px;
  font-weight: bold;
  animation: flash 1.5s linear infinite;
  text-shadow:1px 1px 0 #111, -1px -1px 0 #111,
              -1px 1px 0 #111, 1px -1px 0 #111,
              0px 1px 0 #111,  0-1px 0 #111,
              -1px 0 0 #111, 1px 0 0 #111;
}
.work {
  position: absolute;
  top:60%;
  right: 55%;
  font-size: 20px;
  font-weight: bold;
  animation: flash 1.5s linear infinite;
  text-shadow:1px 1px 0 #111, -1px -1px 0 #111,
              -1px 1px 0 #111, 1px -1px 0 #111,
              0px 1px 0 #111,  0-1px 0 #111,
              -1px 0 0 #111, 1px 0 0 #111;
}
.sns {
  position: absolute;
  bottom: 43%;
  left: 20%;
  font-size: 20px;
  font-weight: bold;
  animation: flash 1.5s linear infinite;
  text-shadow:1px 1px 0 #111, -1px -1px 0 #111,
              -1px 1px 0 #111, 1px -1px 0 #111,
              0px 1px 0 #111,  0-1px 0 #111,
              -1px 0 0 #111, 1px 0 0 #111;
}
.github {
  position: absolute;
  top: 46%;
  right: 12%;
  font-size: 20px;
  font-weight: bold;
  animation: flash 1.5s linear infinite;
  text-shadow:1px 1px 0 #111, -1px -1px 0 #111,
              -1px 1px 0 #111, 1px -1px 0 #111,
              0px 1px 0 #111,  0-1px 0 #111,
              -1px 0 0 #111, 1px 0 0 #111;
}
.exit {
  position: absolute;
  top: 39%;
  right: 0%;
  transform: translate(-50%, -50%);
  font-size: 20px;
  font-weight: bold;
  animation: flash 1.5s linear infinite;
  text-shadow:1px 1px 0 #111, -1px -1px 0 #111,
              -1px 1px 0 #111, 1px -1px 0 #111,
              0px 1px 0 #111,  0-1px 0 #111,
              -1px 0 0 #111, 1px 0 0 #111;
}


@keyframes flash {
	0%,
	100% {
		opacity: 1;
	}

	50% {
		opacity: 0.3;
	}
}




</style>
