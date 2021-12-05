<template>
  <div class="about">
    <div class="messege">
      <h1>Let's Enjoy Sass!</h1>
      <p>
        Sassをご存じですか？<br />
        Sassを使ったことがありますか？<br />
        Sass上級者ですか？
      </p>
    </div>

    <div class="btns">
      <button class="btn">Sassに興味がある！</button>
      <button class="btn">Sassの勉強中！！</button>
      <button class="btn">Sassが大好き！！！</button>
    </div>

    <div class="introductionArea">
      <div class="introduction">
        <h1 class="introTitle">自分が感じるSassの魅力...</h1>
        <p>
          Sassの魅力は、<span class="important">変数</span>や<span
            class="important"
            >マップ型</span
          >を扱うことができることができ、非常に便利だと思います。<br />
          何度も同じ指定をするときなんかは、変数を指定するだけで良いのでとても楽ですね。<br />
          タイプミスによる不具合も減ると思います。
        </p>
        <p class="invitation">皆さんも一緒にSassに挑戦してみませんか？</p>
      </div>
    </div>
  </div>
</template>

<style lang="scss" scoped>
$colors: (
  "mainColor": #4b7eb1,
  "backgroundColor": #edeeef,
  "important": red,
  "title": #004eff,
);
.about {
  background-color: map-get($colors, "backgroundColor");
  height: 90vh;
}

h1 {
  color: map-get($colors, "title");
  margin: 0;
}

.messege {
  width: 640px;
  margin: 0 auto;
  padding: 15px 0 0;
}

.btns {
  width: 640px;
  display: flex;
  justify-content: space-between;
  margin: 0 auto;
  padding: 15px 0;
  .btn {
    width: 30%;
    padding: 16px;
    font-weight: bold;
    border-radius: 10px;
    color: #fff;
    background: map-get($colors, "mainColor");
  }
}

.introductionArea {
  width: 640px;
  margin: 0 auto;
  padding: 15px 0;
  .introduction {
    padding: 15px 30px;
    border: 5px solid map-get($colors, "mainColor");
    .introTitle {
      border-bottom: 2px dashed map-get($colors, "title");
    }
    p {
      text-align: left;
    }
    .invitation {
      text-align: center;
      font-weight: bold;
      font-style: italic;
      color: map-get($colors, "title");
    }
  }
}

.important {
  color: map-get($colors, "important");
}
</style>