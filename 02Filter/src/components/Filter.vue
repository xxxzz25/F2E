<template>
  <el-row>
    <el-col :span="7">
      <div id="filter">
        <div id="location">
          <h2>Location</h2>
          <li v-for="(item,idx) in tagList" :key="idx">
            <input type="checkbox" :id="item.id" v-model="item.isSelected">
            <label :for="item.id" @click.stop="setTags(item)">
              {{item.zone}}
              <span class="count">{{item.contentAmount}}</span>
            </label>
          </li>
        </div>
      </div>
    </el-col>
    <el-col :span="17">
      <router-view/>
    </el-col>
  </el-row>
</template>
<script>
import { mapState, mapMutations } from "vuex";

export default {
  data() {
    return {
      checkList: [],
      date: "",
      tags: []
    };
  },
  computed: {
    ...mapState(["tagList"])
  },
  methods: {
    ...mapMutations(["deleteTag", "setTags"])
  }
};
</script>
<style lang="scss">
@import "../../static/styles/settings.scss";

#filter {
  width: 300px;
  padding: 24px 40px;
  background-color: $color-grey2;
  box-sizing: border-box;
  display: inline-block;
  h2 {
    font-size: 20px;
    font-family: "Roboto-Bold";
  }
  li {
    list-style: none;
    position: relative;
    input[type="checkbox"] {
      display: none;
    }
    label {
      display: inline-block;
      width: 60%;
      margin-left: 40px;
      text-align: center;
      padding: 4px;
      background-color: #fff;
      color: $color-sub;
      border-radius: 2px;
      margin-bottom: 10px;
      transition: 0.3s all;
      border: 1px solid $color-sub;
      cursor: pointer;
    }
    input[type="checkbox"]:checked + label {
      background-color: $color-sub;
      color: #fff;
      transition: 0.3s all;
    }
    .count {
      display: inline-block;
      position: absolute;
      top: 2px;
      right: 0;
      width: 30px;
      height: 30px;
      border: 1px solid $color-sub;
      text-align: center;
      line-height: 30px;
      border-radius: 50%;
    }
  }

  // .el-date-editor {
  //   width: 250px;
  //   margin: 0 auto;
  //   font-size: 16px;
  //   .el-range-separator {
  //     width: auto;
  //   }
  // }
  // .el-checkbox {
  //   display: block;
  //   margin-left: 0;
  //   font-size: 16px;
  //   margin-bottom: 2px;
  // }
}
</style>
