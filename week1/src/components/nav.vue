<template>
  <div class="navi">
    <div class="box">
      <div class="item" v-for="(item,idx) in items" :key="idx">{{item}}</div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      items: ["My tasks", "In Progress", "Completed"]
    };
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="scss">
.navi {
  width: 1024px;
  height: 81px;
  margin: 0 auto;
  background-color: #4a90e2;
  box-sizing: border-box;
  .box {
    width: 660px;
    margin: 0 auto;
    display: flex;
    justify-content: space-around;
    box-sizing: border-box;
    .item {
      width: 220px;
      line-height: 76px;
      color: #00408b;
      font-size: 24px;
      text-align: center;
      &:nth-child(1) {
        color: #fff;
        border-bottom: 5px solid #00408b;
      }
    }
  }
}
</style>
