<template>
  <!-- font -->
  <Head>
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com">
    <link href="https://fonts.googleapis.com/css2?family=DotGothic16&display=swap" rel="stylesheet">
  </Head>
  <!-- app -->
  <v-app>
    <!-- header -->
      <v-app-bar color="#111">
        <v-layout>
          <div class="mx-auto">
            <span class="title"><b>kookeLab</b></span>
            <span class="version"><b>version.1.0.0</b></span>
          </div>
        </v-layout>
      </v-app-bar>
    <!-- contents -->
      <div class="component">
        <!-- lab_image -->
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
        <!-- window-->
          <v-row class="mt-n7">
            <v-col class="d-flex">
              <div class="window-view">
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
                    <v-btn density="compact" variant="outlined" @click="changeFlg(1)">
                      戻る
                    </v-btn>
                  </div>
                  <div class="message" v-else-if="messageFlg == 3">
                    <div class="animate seven">
                      <span>kookeの</span>
                      <span>SKILLは</span>
                      <span>以下の通りです。</span><br><br>
                      <span>■実務経験</span><br>
                      <span>・HTML / </span>
                      <span>CSS / </span>
                      <span>RUBY(RAILS) / </span>
                      <span>NODE.JS(VUE.JS) / </span>
                      <span>MYSQL / </span><br>
                      <span>AWS(S3 /EC2 /ROUTE53 /CLOUDFRONT/ RDS)</span><br><br>
                      <span>■ 個人開発で使ったことがある or 勉強中</span><br>
                      <span>・FIREBASE(HOSTING /REALTIME DATABASE) / </span>
                      <span>REACT(NEXT.JS) / </span>
                      <span>GO / </span>
                      <span>AWS(LAMBDA /DYNAMODB /APIGATEWAY /GRAPHQL)</span><br><br>
                    </div>
                    <v-btn density="compact" variant="outlined" @click="changeFlg(1)">
                      戻る
                    </v-btn>
                  </div>
                  <div class="message" v-else-if="messageFlg == 4">
                    <div class="animate seven">
                      <span>kookeの</span>
                      <span>SNSは</span>
                      <span>以下の通りです。</span><br>
                      <span>Twitter:<a href="https://twitter.com/Koo_Ke" target="_blank">https://twitter.com/Koo_Ke</a></span><br>
                      <span>Qiita:<a href="https://qiita.com/koo-ke" target="_blank">https://qiita.com/koo-ke</a></span><br>
                    </div>
                    <v-btn density="compact" variant="outlined" @click="changeFlg(1)">
                      戻る
                    </v-btn>
                  </div>
                  <div class="message" v-else-if="messageFlg == 5">
                    <div class="animate seven">
                      <span>kookeの</span>
                      <span>WORKは</span>
                      <span>以下の通りです。</span><br><br>
                      <span>2019年 09月 某自社開発会社へ入社。稼働保守チームへ配属。</span><br>
                      <span>2020年 08月 稼働保守チームの調査システムを開発。</span><br>
                      <span>2020年 10月 web開発チームへ異動。</span><br>
                      <span>2021年 12月 新規アプリのfront担当。</span><br>
                      <span>2022年 03月 SSH接続を駆使した調査システムを作成。</span><br>
                      <span>2022年 05月 社内アプリのUIを一新。</span><br>
                      <span>2023年 02月 新規アプリの開発を担当。</span><br><br>
                    </div>
                    <v-btn density="compact" variant="outlined" @click="changeFlg(1)">
                      戻る
                    </v-btn>
                  </div>
                  <div class="message" v-else-if="messageFlg == 6">
                    <div class="animate seven">
                      <span>kookeの</span>
                      <span>GitHubを</span>
                      <span>表示しますか？</span>
                    </div>
                    <v-btn variant="outlined" density="compact" href="https://github.com/koo-ke" target="_blank">
                      はい
                    </v-btn>
                    <v-btn density="compact" variant="outlined" @click="changeFlg(1)">
                      いいえ
                    </v-btn>
                  </div>
                </div>
              </div>
            </v-col>
          </v-row>
          <div class="release-notes">
            Release notes 1.0.0 2023/04/25 PC版ビュー作成
          </div>
      </div>
  </v-app>
</template>

<script setup lang="ts">
  // メッセージウインドウの分岐
  let messageFlg = ref(1)
  const changeFlg = (flg:number) => {
    messageFlg.value = flg
  }
</script>

<style>
/* フォント指定 */
  .v-application{
    font-family: 'DotGothic16', sans-serif;
  }

/* メッセージウインドウのアニメーション */
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

  .release-notes {
    display: flex;
    width: 100%;
    margin: 0 auto 0 auto;
    max-width: 820px;
    color:white;
    font-size: 10px;
  }


/* キャラクターとメッセージの段落 */
  .window-view {
    display: flex;
    width: 100%;
    margin: 0 auto 0 auto;
    max-width: 820px;
  }

/* キャラクターウインドウ */
  .character-window {
    width: 120px;
  }

/* メッセージウインドウ */
  .message-window {
    width: 100%;
    height: 158px;
    background-color: white;
    padding: 5px;
    overflow:scroll
  }
  .message-window::-webkit-scrollbar{
    display: none;
  }

/* ヘッダーに出すタイトル */
  .title {
    font-size: 40px;
    text-shadow:1px 1px 0 #999, -1px -1px 0 #999,
                -1px 1px 0 #999, 1px -1px 0 #999,
                0px 1px 0 #111,  0-1px 0 #111,
                -1px 0 0 #111, 1px 0 0 #111;
  }

/* バージョン */
  .version {
    margin-left: 10px;
    font-size: 20px;
    color: white;
  }

/* コンテンツワッパー */
  .component {
    margin: 0 auto 0 auto;
    padding: 60px 5% 5% 5%;
    background-color: #111;
    height: 100vh;
    width: 100%;
  }

/* ラボイメージ & 中の文字 */
  .lab {
    width: 90%;
    margin: 0 auto 0 auto;
    margin-top: 20px;
    max-width: 820px;
  }
  .box img {
    width: 100%;
    height: auto;
  }
  p {
    margin: 0;
    padding: 0;
    color: #FFF;
    font-size: 32px;
  }
  .box{
    position: relative;
  }

/* 中の文字のポジションと、リンク範囲のポジション */
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
    top: 30%;
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
    top: 55%;
    left: 17%;
    width: 9%;
    height: 15%;
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
    top: 63%;
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
    top: 50%;
    left: 76%;
    width: 10%;
    height: 14%;
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

/* リンク文字のアニメーション */
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
