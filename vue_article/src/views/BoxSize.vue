<template>
  <div class="boxSize">
    <p>Boxの高さを調査してみよう！</p>
    <div class="box" ref="box">
      <span>Box</span>
    </div>
  </div>
</template>

<script>
import { onMounted, ref } from "vue";
export default {
  name: "BoxSize",
  setup() {
    const box = ref();

    console.log(box.value);

    onMounted(() => {
      console.log(box.value); // <div class="box" data-v-2fce3522>...</div>

      // 要素のサイズ・位置を求める。
      const boxSize = box.value.getBoundingClientRect();
      console.log(boxSize);

      // 幅
      const boxWidth = boxSize.width;
      console.log(boxWidth); // 150

      // 高さ
      const boxHeight = boxSize.height;
      console.log(boxHeight); // 120
    });

    return {
      box,
    };
  },
};
</script>

<style lang="scss" scoped>
.box {
  width: 150px;
  height: 120px;
  background-color: #edeeef;
  display: flex;
  justify-content: center;
  align-items: center;
  margin: 0 auto;
  span {
    font-weight: bold;
    color: #004eff;
  }
}
</style>