<template>
  <div class="home">
    <h1>Sassを使ってみよう！</h1>
    <h2>変数を使ってみよう！</h2>
    <p class="color1">文字色1</p>
    <p class="color2">文字色2</p>
    <p class="color3">文字色3</p>
    <hr />
    <h2>変数便利！</h2>
    <p class="color1">文字色1</p>
    <p class="color2">文字色2</p>
    <p class="color3">文字色3</p>
  </div>
</template>

<script>
export default {
  name: "Home",
};
</script>

<style lang="scss" scoped>
$colorH1: #0000ff;
$colorH2: #000;
$color1: #9999ff;
$color2: #6666ff;
$color3: #0000cc;

h1 {
  color: $colorH1;
}

h2 {
  color: $colorH2;
}

.color1 {
  color: $color1;
}

.color2 {
  color: $color2;
}

.color3 {
  color: $color3;
}

hr {
  border-color: $colorH1;
}
</style>
