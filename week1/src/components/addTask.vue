<template>
<div class="container">
  <div class="addTask" @click="isNewtodo = true" v-if="isNewtodo === false">+ Add Task</div>
  <div class="addItem" v-if="isNewtodo === true">
    <div class="top">
      <div class="box">
        <input type="text" value="Type Something Here..." v-model="cacheTodo.title">
        <div class="right">
          <span>
            <i class="far fa-star" @click="list.star=!list.star"></i>
          </span>
          <i class="far fa-edit"></i>
      </div>
      </div>
    </div>
    <div class="content">
      <div class="item">
        <div class="text">
          <i class="far fa-calendar-alt"></i>
          Deadline
        </div>
        <div class="data">
          <input type="datetime-local" v-model="cacheTodo.date">
        </div>
      </div>
      <div class="item">
        <div class="text">
          <i class="far fa-file"></i>
          File
        </div>
        <div class="data">
          <input type="file">
        </div>
      </div>
      <div class="item">
        <div class="text">
          <i class="far fa-comments"></i>
          Comment
        </div>
        <div class="data">
          <textarea cols="30" rows="10" v-model="cacheTodo.comment"></textarea>
        </div>
      </div>
    </div>
    <div class="bottom">
      <div class="item" @click="isNewtodo = false">X Cancel</div>
      <div class="item" @click="updateTodo">+ Save</div>
    </div>
  </div>
</div>
  
</template>

<script>
export default {
  data() {
    return {
      isNewtodo: false,
      cacheTodo: {
        title: "",
        fileList: "",
        date: "",
        comment: "",
        status: false,
        star: false
      }
    };
  },
  methods: {
    updateTodo() {
      this.$bus.$emit("update", this.cacheTodo);
      this.cacheTodo = {
        title: "",
        fileList: "",
        date: "",
        comment: "",
        status: false,
        star: false
      };
      this.isNewtodo = false;
    }
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="scss">
.addTask {
  box-sizing: border-box;
  margin: 0 auto;
  margin-top: 30px;
  width: 620px;
  height: 65px;
  border-radius: 5px;
  background-color: #fff;
  border: 2px solid #c8c8c8;
  display: flex;
  align-items: center;
  color: #c8c8c8;
  padding-left: 30px;
  font-size: 24px;
}
input {
  box-sizing: border-box;
  border-radius: 5px;
}
.addItem {
  width: 620px;
  margin: 0 auto;
  margin-top: 30px;
  box-shadow: 0 4px 4px 0 #c8c8c8;
  .top {
    line-height: 76px;
    background-color: #fff2dc;
    font-size: 24px;
    border-radius: 5px 5px 0 0;
    .box {
      margin-left: 96px;
      input {
        width: 350px;
        height: 40px;
      }
      .right {
        float: right;
        margin-right: 50px;
        span{
          margin-right: 15px;
        }
      }
    }
  }
  .content {
    padding: 20px 0;
    background-color: #f2f2f2;
    .item {
      width: 465px;
      margin: 0 auto;
      margin-top: 20px;
      .text {
        font-size: 20px;
      }
      .data {
        margin-left: 20px;
        textarea {
          width: 465px;
          resize: none;
        }
      }
    }
  }
  .bottom {
    height: 60px;
    display: flex;
    border-radius: 0 0 5px 5px;
    justify-content: space-around;
    .item {
      width: 100%;
      font-size: 24px;
      line-height: 60px;
      text-align: center;
      border-radius: 0 0 5px 5px;
      &:first-child {
        background-color: #fff;
        color: #d0021b;
      }
      &:last-child {
        background-color: #4a90e2;
        color: #fff;
      }
    }
  }
}
</style>
