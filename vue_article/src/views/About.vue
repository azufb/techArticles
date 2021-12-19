<template>
  <div class="about">
    <div class="messege">
      <h1>Let's Enjoy Sass!</h1>
      <p>Sassのマップ型を使ってみる。</p>
    </div>

    <div class="btns">
      <button class="btn">Sassに興味がある！</button>
      <button class="btn">Sass勉強中！！</button>
      <button class="btn">Sass大好き！！！</button>
    </div>
  </div>
</template>

<script>
export default {
  name: "About",
  setup() {
    console.log(location.pathname);
    console.log(location);
    console.log(history);
    console.log(history.state);
    console.log(history.state.back);
  },
};
</script>

<style lang="scss" scoped>
$colors: (
  "mainColor": #4b7eb1,
  "backgroundColor": #edeeef,
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
</style>