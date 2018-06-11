<template>
<div class="container">
  <div 
    class="todoItem"
    :class="{starItem: list.star, statusItem: list.status}" 
    v-for="(list, idx) in lists" 
    :key="idx"
  >
    <div class="box">
      <input type="checkbox"  v-model="list.status">
      <span :class="list.status? 'line':''">{{list.title}}</span>
      <div class="right">
        <span>
          <i class="far fa-star" @click="list.star=!list.star" v-if="list.star==false"></i>
          <i class="fas fa-star" @click="list.star=!list.star" v-else></i>
        </span>
        <i class="far fa-edit"></i>
      </div>
    </div>
  </div>
</div>
  
</template>

<script>
export default {
  data() {
    return {
      lists: [
        {
          title: "Go 87",
          fileList: "",
          date: "",
          comment: "qqq",
          status: false,
          star: false
        },
        {
          title: "Go 879487",
          fileList: "",
          date: "",
          comment: "qqq",
          status: false,
          star: true
        },
        {
          title: "Go Go Go",
          fileList: "",
          date: "",
          comment: "hahaha",
          status: false,
          star: false
        }
      ]
    };
  },
  created() {
    //註冊監聽事件
    this.$bus.$on("update", e => {
      this.lists.push(e);
    });
  },
  beforeDestroy() {
    //銷毀監聽事件，最好在組件銷毀前清除specialEvent所有監聽
    //如果要指定哪個監聽對應方法，就需要傳入第二個參數(對應$on設定的方法)
    this.$bus.$off("update");
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="scss">
.container {
  display: flex;
  flex-wrap: wrap;
  .todoItem {
    width: 620px;
    margin: 0 auto;
    margin-top: 30px;
    line-height: 76px;
    border-radius: 5px;
    background-color: #fff;
    font-size: 24px;
    box-shadow: 0 4px 4px 0 #c8c8c8;
    .box {
      margin-left: 96px;
      .line {
        text-decoration: line-through;
      }
      .right {
        float: right;
        margin-right: 50px;
        span {
          margin-right: 15px;
          .fas {
            color: #F5A623;
          }
        }
      }
    }
  }
  .todoItem.starItem {
    background-color: #fff2dc;
    order: -1;
  }
  .todoItem.statusItem {
    order: 999;
  }
}
</style>
