<template>

  <Head>
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com">
    <link href="https://fonts.googleapis.com/css2?family=DotGothic16&display=swap" rel="stylesheet">
  </Head>


  <v-app>

    <!-- header -->
      <v-app-bar color="#111">
        <v-layout>
          <div class="mx-auto">
            <span class="title"><b>kookeLab</b></span>
            <span class="version"><b>version.0.0.1</b></span>
          </div>
        </v-layout>
      </v-app-bar>


    <!-- contents01 -->
      <div class="component-01">

          <v-row>
            <v-col class="d-flex">
              <div class="mx-auto">
                <div class="box">
                  <img class="lab" src="@/assets/image/lab.png">
                  <p class="skill">
                    ▼ SKILL
                  </p>
                  <p class="skill-box" @click="changeFlg(3)"></p>
                  <p class="sns">
                    ▼ SNS
                  </p>
                  <p class="sns-box" @click="changeFlg(4)"></p>
                  <p class="chat">
                    ▼ Chat
                  </p>
                  <p class="work">
                    ▼ WORK
                  </p>
                  <p class="work-box" @click="changeFlg(5)"></p>
                  <p class="game">
                    ▼ Game
                  </p>
                  <p class="github">
                    ▼ GitHub
                  </p>
                  <p class="github-box" @click="changeFlg(6)"></p>
                </div>
              </div>
            </v-col>
          </v-row>

          <v-row class="mt-n7">
            <v-col class="d-flex">
              <div class="aaa">
                <div class="character-window">
                  <img width="120" src="@/assets/image/avatar.png">
                </div>


                <div class="message-window">
                  <b>【kooke】</b><br>

                  <div class="message" v-if="messageFlg == 1">
                    <div class="animate seven">
                      <span>kooke</span>
                      <span>Labへ</span>
                      <span>ようこそ。</span>
		                </div>
                    <v-btn density="compact" variant="outlined" @click="changeFlg(2)">
                      ここはなんですか?
                    </v-btn>
                  </div>

                  <div class="message" v-else-if="messageFlg == 2">
                    <div class="animate seven">
                      <span>ここは</span>
                      <span>エンジニア</span>
                      <span>kookeの</span>
                      <span>ポートフォリオ</span>
                      <span>サイトです。</span><br>
                      <span>各種</span>
                      <span>項目を</span>
                      <span>選んで</span>
                      <span>頂くと</span>
                      <span>kookeに</span>
                      <span>ついて</span>
                      <span>確認</span>
                      <span>することが</span>
                      <span>出来ます。</span>
		                </div>
                  </div>

                  <div class="message" v-else-if="messageFlg == 3">
                    skill
                  </div>

                  <div class="message" v-else-if="messageFlg == 4">
                    sns
                  </div>

                  <div class="message" v-else-if="messageFlg == 5">
                    work
                  </div>

                  <div class="message" v-else-if="messageFlg == 6">
                    kookeのGitHubを表示しますか？
                    <v-btn variant="outlined" density="compact" href="https://github.com/koo-ke" target="_blank">
                      お願いします！
                    </v-btn>
                  </div>

                </div>



              </div>
            </v-col>
          </v-row>
      </div>




      


  </v-app>
</template>

<script setup lang="ts">
  let messageFlg = ref(1)
  const changeFlg = (flg:number) => {
    messageFlg.value = flg
  }
</script>

<style>





.animate span {
	display: inline-block;
}

.animate span:nth-of-type(2) {
	animation-delay: .05s;
}
.animate span:nth-of-type(3) {
	animation-delay: .1s;
}
.animate span:nth-of-type(4) {
	animation-delay: .15s;
}
.animate span:nth-of-type(5) {
	animation-delay: .2s;
}
.animate span:nth-of-type(6) {
	animation-delay: .25s;
}
.animate span:nth-of-type(7) {
	animation-delay: .3s;
}
.animate span:nth-of-type(8) {
	animation-delay: .35s;
}
.animate span:nth-of-type(9) {
	animation-delay: .4s;
}
.animate span:nth-of-type(10) {
	animation-delay: .45s;
}
.animate span:nth-of-type(11) {
	animation-delay: .5s;
}
.animate span:nth-of-type(12) {
	animation-delay: .55s;
}
.animate span:nth-of-type(13) {
	animation-delay: .6s;
}
.animate span:nth-of-type(14) {
	animation-delay: .65s;
}
.animate span:nth-of-type(15) {
	animation-delay: .7s;
}
.animate span:nth-of-type(16) {
	animation-delay: .75s;
}
.animate span:nth-of-type(17) {
	animation-delay: .8s;
}
.animate span:nth-of-type(18) {
	animation-delay: .85s;
}
.animate span:nth-of-type(19) {
	animation-delay: .9s;
}
.animate span:nth-of-type(20) {
	animation-delay: .95s;
}

.seven span {
	opacity: 0;
	transform: translate(-150px, 0) scale(.3);
	animation: leftRight .5s forwards;
}

@keyframes leftRight {
	40% {
		transform: translate(50px, 0) scale(.7);
		opacity: 1;
	}

	60% {
		color: #888;
	}

	80% {
		transform: translate(0) scale(2);
		opacity: 0;
	}

	100% {
		transform: translate(0) scale(1);
		opacity: 1;
	}
}


















.aaa {
  display: flex;
  width: 100%;
  margin: 0 auto 0 auto;
  max-width: 820px;
}

.character-window {
  width: 120px;
}

.message-window {
  width: 100%;
  background-color: white;
  padding: 5px;
  height: 100%;
}


.title {
  font-size: 40px;
  text-shadow:1px 1px 0 #999, -1px -1px 0 #999,
              -1px 1px 0 #999, 1px -1px 0 #999,
              0px 1px 0 #111,  0-1px 0 #111,
              -1px 0 0 #111, 1px 0 0 #111;
}

.version {
  margin-left: 10px;
  font-size: 20px;
  color: white;
}


















  /* フォント */
  .v-application{
    font-family: 'DotGothic16', sans-serif;
  }

  /* contents01 */
  .component-01 {
    margin: 0 auto 0 auto;
    padding: 60px 5% 5% 5%;
    background-color: #111;
    height: 100vh;
    width: 100%;
  }


  .lab {
    width: 90%;
    margin: 0 auto 0 auto;
    margin-top: 20px;
    max-width: 820px;
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
  top: 29%;
  left: 11%;
  font-size: 20px;
  font-weight: bold;
  animation: flash 1.5s linear infinite;
  text-shadow:1px 1px 0 #111, -1px -1px 0 #111,
              -1px 1px 0 #111, 1px -1px 0 #111,
              0px 1px 0 #111,  0-1px 0 #111,
              -1px 0 0 #111, 1px 0 0 #111;
}
.skill-box {
  position: absolute;
  top: 35%;
  left: 9%;
  width: 14%;
  height: 20%;
  background-color: white;
  opacity: 0;
  cursor: pointer;
}


.sns {
  position: absolute;
  top: 54%;
  left: 20%;
  font-size: 20px;
  font-weight: bold;
  animation: flash 1.5s linear infinite;
  text-shadow:1px 1px 0 #111, -1px -1px 0 #111,
              -1px 1px 0 #111, 1px -1px 0 #111,
              0px 1px 0 #111,  0-1px 0 #111,
              -1px 0 0 #111, 1px 0 0 #111;
}
.sns-box {
  position: absolute;
  top: 60%;
  left: 17%;
  width: 7%;
  height: 10%;
  background-color: white;
  opacity: 0;
  cursor: pointer;
}




.work {
  position: absolute;
  top:60%;
  left: 35%;
  font-size: 20px;
  font-weight: bold;
  animation: flash 1.5s linear infinite;
  text-shadow:1px 1px 0 #111, -1px -1px 0 #111,
              -1px 1px 0 #111, 1px -1px 0 #111,
              0px 1px 0 #111,  0-1px 0 #111,
              -1px 0 0 #111, 1px 0 0 #111;
}
.work-box {
  position: absolute;
  top: 67%;
  left: 28%;
  width: 25%;
  height: 15%;
  background-color: white;
  opacity: 0;
  cursor: pointer;
}


.chat {
  color: #777;
  position: absolute;
  top:21%;
  left: 35%;
  font-size: 20px;
  font-weight: bold;
  text-shadow:1px 1px 0 #111, -1px -1px 0 #111,
              -1px 1px 0 #111, 1px -1px 0 #111,
              0px 1px 0 #111,  0-1px 0 #111,
              -1px 0 0 #111, 1px 0 0 #111;
}

.game {
  color: #777;
  position: absolute;
  top:40%;
  left: 64%;
  font-size: 20px;
  font-weight: bold;
  text-shadow:1px 1px 0 #111, -1px -1px 0 #111,
              -1px 1px 0 #111, 1px -1px 0 #111,
              0px 1px 0 #111,  0-1px 0 #111,
              -1px 0 0 #111, 1px 0 0 #111;
}



.github {
  position: absolute;
  top: 49%;
  left: 78%;
  font-size: 20px;
  font-weight: bold;
  animation: flash 1.5s linear infinite;
  text-shadow:1px 1px 0 #111, -1px -1px 0 #111,
              -1px 1px 0 #111, 1px -1px 0 #111,
              0px 1px 0 #111,  0-1px 0 #111,
              -1px 0 0 #111, 1px 0 0 #111;
}
.github-box {
  position: absolute;
  top: 55%;
  left: 76%;
  width: 7%;
  height: 9%;
  background-color: white;
  opacity: 0;
  cursor: pointer;
}

.ｍessage {
  position: absolute;
  top: 46%;
  left: 78%;
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
