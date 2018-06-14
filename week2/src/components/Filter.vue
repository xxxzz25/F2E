<template>
  <div class="fun">
      <div class="top">
        <div class="logo">
          HaveFun
        </div>
        <div class="search">
          <i class="fas fa-search"></i>
        <input type="text" placeholder="Explore your own activities">
        </div>
      </div>

      <div class="left">
        <div class="container">
          <div class="text">
            Location
          </div>
          <select>
            <option>Taiwan</option>
            <option>Japan</option>
          </select>
        </div>
        <div class="container">
          <div class="text">
            Date
          </div>
          <div class="content">
            <div class="box">
              <div class="date_left">from</div>
              <div class="date_right">
                <input type="date">
              </div>
            </div>
            <div class="box">
              <div class="date_left">to</div>
              <div class="date_right">
                <input type="date">
              </div>
            </div>
          </div>
        </div>
        <div class="container">
          <div class="text">
            Categories
          </div>
          <div class="content">
            <li>
              <input type="checkbox" multiple id="data1">
              <label for="data1">All</label>
            </li>
            <li>
              <input type="checkbox" multiple id="data2">
              <label for="data2">Entertainment</label>
            </li>
            <li>
              <input type="checkbox" multiple id="data3">
              <label for="data3">Food</label>
            </li>
            <li>
              <input type="checkbox" multiple id="data4">
              <label for="data4">Learning</label>
            </li>
            <li>
              <input type="checkbox" multiple id="data5">
              <label for="data5">Outdoors</label>
            </li>
          </div>
        </div>
      </div>

      <div class="right">
        <div class="result">
          <div class="text">
            Showing <span>15</span> results by...
          </div>
          <div class="btn">
            <div class="item">
              Koahsiung
              <i class="far fa-times-circle"></i>
            </div>
            <div class="item">
              Entertainment
              <i class="far fa-times-circle"></i>
            </div>
          </div>
        </div>
        <div class="show">
          <div class="item">
            <div class="pic"></div>
            <div class="text">
              <div class="title">Kogi Cosby sweater</div>
              <div class="content">
                Donec euismod scelerisque ligula. Maecenas eu varius risus, eu aliquet arcu. Curabitur fermentum suscipit est, tincidunt mattis lorem luctus id. Donec eget massa a diam condimentum pretium. Aliquam erat volutpat. Integer ut tincidunt orci. Etiam tristique, elit ut consectetur iaculis, metus lectus mattis justo, vel mollis eros neque quis augue. Sed lobortis ultrices lacus, a placerat metus rutrum sit amet. Aenean ut suscipit justo.v
              </div>
              <div class="author">
                <div class="name">Ethan Foster</div>
                <div class="type">Entertainment</div>
              </div>
              <div class="place">
                <div class="city">
                  <i class="fas fa-map-marker-alt"></i>
                  Kaohsiung City
                </div>
                <div class="date">
                  <i class="far fa-calendar-alt"></i>
                  2018/5/24 - 2018/5/31
                </div>
              </div>
            </div>
          </div>
          <div class="item">
            <div class="pic"></div>
            <div class="text">
              <div class="title">Kogi Cosby sweater</div>
              <div class="content">
                Donec euismod scelerisque ligula. Maecenas eu varius risus, eu aliquet arcu. Curabitur fermentum suscipit est, tincidunt mattis lorem luctus id. Donec eget massa a diam condimentum pretium. Aliquam erat volutpat. Integer ut tincidunt orci. Etiam tristique, elit ut consectetur iaculis, metus lectus mattis justo, vel mollis eros neque quis augue. Sed lobortis ultrices lacus, a placerat metus rutrum sit amet. Aenean ut suscipit justo.v
              </div>
              <div class="author">
                <div class="name">Ethan Foster</div>
                <div class="type">Entertainment</div>
              </div>
              <div class="place">
                <div class="city">
                  <i class="fas fa-map-marker-alt"></i>
                  Kaohsiung City
                </div>
                <div class="date">
                  <i class="far fa-calendar-alt"></i>
                  2018/5/24 - 2018/5/31
                </div>
              </div>
            </div>
          </div>
          <div class="item">
            <div class="pic"></div>
            <div class="text">
              <div class="title">Kogi Cosby sweater</div>
              <div class="content">
                Donec euismod scelerisque ligula. Maecenas eu varius risus, eu aliquet arcu. Curabitur fermentum suscipit est, tincidunt mattis lorem luctus id. Donec eget massa a diam condimentum pretium. Aliquam erat volutpat. Integer ut tincidunt orci. Etiam tristique, elit ut consectetur iaculis, metus lectus mattis justo, vel mollis eros neque quis augue. Sed lobortis ultrices lacus, a placerat metus rutrum sit amet. Aenean ut suscipit justo.v
              </div>
              <div class="author">
                <div class="name">Ethan Foster</div>
                <div class="type">Entertainment</div>
              </div>
              <div class="place">
                <div class="city">
                  <i class="fas fa-map-marker-alt"></i>
                  Kaohsiung City
                </div>
                <div class="date">
                  <i class="far fa-calendar-alt"></i>
                  2018/5/24 - 2018/5/31
                </div>
              </div>
            </div>
          </div>
          <div class="page">
            <div class="item"><i class="fas fa-angle-double-left"></i></div>
            <div class="item">1</div>
            <div class="item">2</div>
            <div class="item">3</div>
            <div class="item">4</div>
            <div class="item">5</div>
            <div class="item"><i class="fas fa-angle-double-right"></i></div>
          </div>
        </div>
      </div>

  </div>
</template>

<script>
export default {
  data() {
    return {
      msg: "Welcome to Your Vue.js App"
    };
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="scss" scoped>
.fun {
  width: 1200px;
  margin: 0 auto;
  background-color: #f2f2f2;
  &:after {
    content: "";
    display: block;
    clear: both;
  }
  .top {
    width: 100%;
    height: 92px;
    background-color: #7828b4;
    display: flex;
    align-items: center;
    .logo {
      width: 157px;
      font-family: "Optima-ExtraBlack","arial";
      color: #fff;
      font-size: 36px;
      line-height: 45px;
      margin-left: 78px;
    }
    .search {
      margin-left: 149px;
      font-size: 20px;
      width: 388px;
      padding-bottom: 5px;
      padding-left: 5px;
      border-bottom: 2px solid #fff;
      color: #fff;
      input {
        width: 255px;
        margin-left: 25px;
        font-family: "Roboto-Italic","arial";
        font-style: italic;
        border: none;
        background-color: transparent;
        outline: none;
        color: #fff;
        font-size: 20px;
        &::placeholder {
          color: rgba(255, 255, 255, 0.5);
        }
      }
    }
  }
  .left {
    width: 300px;
    background-color: #ebebeb;
    margin-left: 38px;
    box-sizing: border-box;
    font-family: "Roboto-Regular","arial";
    float: left;
    .container {
      padding: 24px 40px;
      border-bottom: 1px solid #d7d7d7;
      .text {
        font-family: "Roboto-Bold","arial";
        font-weight: bold;
        font-size: 20px;
        color: #000000;
        margin-bottom: 15px;
      }
      &:nth-child(1) {
        select {
          width: 220px;
          height: 40px;
        }
      }
      &:nth-child(2) {
        .content {
          width: 216px;
          .box {
            display: flex;
            margin-bottom: 8px;
            align-items: center;
            .date_left {
              width: 34px;
              margin-right: 13px;
              text-align: right;
              font-size: 16px;
            }
            .date_right {
              width: 169px;
              input {
                height: 40px;
              }
            }
          }
        }
      }
      &:nth-child(3) {
        .content {
          list-style: none;
          li {
            display: flex;
            align-items: center;
            margin-bottom: 8px;
            input[type="checkbox"] {
              appearance: none;
              border: none;
              width: 16px;
              height: 16px;
              background-color: #fff;
              margin-right: 6px;
              border-radius: 2px;
              display: flex;
              align-items: center;
              justify-content: center;
              &:after{
                display: block;
                content: '✔';
                color: #fff;
              }
              &:checked{
                background-color: #7828b4;
              }
              &:focus{
                outline: none;
              }
            }
          }
        }
      }
    }
  }
  .right {
    box-sizing: border-box;
    padding: 24px 40px;
    float: left;
    .result {
      margin-bottom: 24px;
      .text {
        margin-bottom: 24px;
        font-family: "Roboto-Regular","arial";
        font-size: 24px;
        span {
          color: #9013fe;
          font-weight: bold;
        }
      }
      .btn {
        display: flex;
        .item {
          margin-right: 8px;
          border: 1px solid #9013fe;
          border-radius: 100px;
          font-size: 16px;
          font-style: italic;
          padding: 8px;
          color: #9013fe;
          cursor: pointer;
        }
      }
    }
    .show {
      width: 780px;
      .item {
        width: 100%;
        display: flex;
        margin-bottom: 24px;
        transition: all .7s;
        cursor: pointer;
        &:hover{
          box-shadow: 5px 8px 3px #888;
        }
        .pic {
          width: 220px;
          height: 220px;
          background-color: #9013FE;
        }
        .text {
          box-sizing: border-box;
          width: 560px;
          padding: 24px 20px;
          font-size: 16px;
          font-family: "Roboto-Regular","arial";
          background-color: #fff;
          .title {
            font-family: "Roboto-Bold", "arial","arial";
            font-weight: bold;
            font-size: 24px;
            color: #9013fe;
            line-height: 36px;
            margin-bottom: 16px;
          }
          .content {
            height: 50px;
            overflow: hidden;
            margin-bottom: 13px;
          }
          .author {
            display: flex;
            align-items: center;
            margin-bottom: 14px;
            .name {
              font-family: "Roboto-Bold","arial";
              font-weight: bold;
              margin-right: 20px;
            }
            .type {
              background: #d7d7d7;
              border-radius: 100px;
              padding: 3px 16px;
              color: #fff;
              font-style: italic;
            }
          }
          .place {
            display: flex;
            color: #9b9b9b;
            i {
              margin-right: 7px;
              color: #000;
            }
            .city {
              margin-right: 20px;
            }
          }
        }
      }
      .page{
        display: flex;
        float: right;
        .item{
          width: 42px;
          height: 42px;
          background-color: #fff;
          color: #9013FE;
          border: 1px solid #ECEEEF;
          border-radius: 4px;
          display: flex;
          justify-content: center;
          align-items: center;
          font-size: 16px;
          font-family: "HelveticaNeue","arial";
          &:hover{
            box-shadow: none;
            background-color:#9013FE;
            color: #fff;
          }
          &:nth-child(2){
            background-color:#9013FE;
            color: #fff;
          }
        }
      }
    }
  }
}
</style>

