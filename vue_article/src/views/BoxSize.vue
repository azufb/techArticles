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
    const box = ref(null);

    onMounted(() => {
      console.log(box.value);
      const boxSize = box.value.getBoundingClientRect();
      const boxWidth = boxSize.width;
      const boxHeight = boxSize.height;
      console.log(`Boxの幅：${boxWidth}`);
      console.log(`Boxの高さ：${boxHeight}`);
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