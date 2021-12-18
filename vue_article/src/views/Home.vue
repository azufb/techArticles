<template>
  <div class="home">
    <h1>Sassを使ってみよう！</h1>
    <h2>変数を使ってみよう！</h2>
    <p class="color1">文字色1</p>
    <p class="color2">文字色2</p>
    <p class="color3">文字色3</p>
    <hr />
  </div>
</template>

<script>
export default {
  name: "Home",
};
</script>

<style lang="scss" scoped>
$blue1: #0000ff;
$black: #000;
$blue2: #9999ff;
$blue3: #6666ff;
$blue4: #0000cc;

h1 {
  color: $blue1;
}

h2 {
  color: $black;
}

.color1 {
  color: $blue2;
}

.color2 {
  color: $blue3;
}

.color3 {
  color: $blue4;
}

hr {
  border-color: $blue1;
}
</style>
