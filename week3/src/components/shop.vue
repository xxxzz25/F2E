<template>
  <div>
    <div class="nav">
      <div class="container">
        <div class="logo">Shoptime</div>
        <div class="box">
          <div class="item">HOME</div>
          <div class="item">ORDERS</div>
          <div class="item">PRODUCT</div>
        </div>
        <div class="login">ADMIN</div>
      </div>
    </div>

    <div class="content">
      <div class="container">
        <div class="top">
          <div class="left">OVERVIEW</div>
          <div class="right">
            <span>2018/6/6 <i class="fas fa-caret-right"></i> 2018/6/13</span>
            <select>
              <option>Weekly</option>
              <option>Monthly</option>
              <option>Yearly</option>
            </select>
          </div>
        </div>
        <div class="num">
          <div class="item">
            <div class="text">
              <i class="fas fa-hand-holding-usd"></i>
              TOTAL REVENUE
            </div>
            <div class="number">54540</div>
          </div>
          <div class="item">
            <div class="text">
              <i class="fas fa-boxes"></i>
              TOTAL COST
            </div>
            <div class="number">12660</div>
          </div>
          <div class="item">
            <div class="text">
              <i class="fas fa-money-bill"></i>
              NET INCOME
            </div>
            <div class="number">41880</div>
          </div>
        </div>
        <div class="line"></div>
        <div class="product">
          <div class="left">
            <div class="title">
              Transaction Website
            </div>
            <div class="item">
              <div class="icon">
                <i class="fab fa-facebook"></i>
              </div>
              <div class="com">
                Facebook.com
              </div>
              <div class="count">
                45,836
              </div>
              <div class="percent">
                <i class="fas fa-arrow-up"></i>20%
              </div>
            </div>
            <div class="item">
              <div class="icon">
                <i class="fab fa-google"></i>
              </div>
              <div class="com">
                google.com
              </div>
              <div class="count">
                23,582
              </div>
              <div class="percent">
                <i class="fas fa-arrow-up"></i>12%
              </div>
            </div>
            <div class="item">
              <div class="icon">
                <i class="fas fa-shopping-bag"></i>
              </div>
              <div class="com">
                Shopify.com
              </div>
              <div class="count">
                2,489
              </div>
              <div class="percent">
                <i class="fas fa-arrow-down"></i>15%
              </div>
            </div>
            <div class="item">
              <div class="icon">
                <i class="fab fa-wordpress"></i>
              </div>
              <div class="com">
                Wordpress.com
              </div>
              <div class="count">
                1,057
              </div>
              <div class="percent">
                <i class="fas fa-arrow-down"></i>30%
              </div>
            </div>
          </div>
          <div class="right">
            <div class="title">
              Latest Orders
            </div>
            <div class="item">
              <div class="pic"></div>
              <div class="text">
                <div class="itemName">Cowboy Jacket</div>
                <div class="date">
                  <i class="fas fa-clock"></i>
                  2018/6/13  13:42
                </div>
                <div class="name">
                  <i class="fas fa-male"></i>
                  Lura Holland
                </div>
              </div>
              <div class="total">
                <div class="totalText">Total</div>
                <div class="totalNum">3200</div>
              </div>
            </div>
            <div class="item">
              <div class="pic"></div>
              <div class="text">
                <div class="itemName">Cowboy Jacket</div>
                <div class="date">
                  <i class="fas fa-clock"></i>
                  2018/6/13  13:42
                </div>
                <div class="name">
                  <i class="fas fa-male"></i>
                  Lura Holland
                </div>
              </div>
              <div class="total">
                <div class="totalText">Total</div>
                <div class="totalNum">3200</div>
              </div>
            </div>
            <div class="item">
              <div class="pic"></div>
              <div class="text">
                <div class="itemName">Cowboy Jacket</div>
                <div class="date">
                  <i class="fas fa-clock"></i>
                  2018/6/13  13:42
                </div>
                <div class="name">
                  <i class="fas fa-male"></i>
                  Lura Holland
                </div>
              </div>
              <div class="total">
                <div class="totalText">Total</div>
                <div class="totalNum">3200</div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {};
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="scss">
.nav {
  width: 1024px;
  margin: 0 auto;
  background-color: #000;
  color: #fff;
  font-weight: bold;
  .container {
    padding: 21px 42px;
    &:after {
      content: "";
      display: block;
      clear: both;
    }
    .logo {
      font-size: 24px;
      float: left;
    }
    .box {
      float: left;
      display: flex;
      align-items: center;
      font-size: 16px;
      margin-left: 65px;
      position: relative;
      .item {
        width: 80px;
        margin: 0 25px;
        text-align: center;
        line-height: 24px;
        color: #9b9b9b;
        &:first-child {
          color: #fff;
          &:after {
            content: "";
            display: block;
            width: 80px;
            height: 4px;
            position: absolute;
            top: 44px;
            background-color: #fff;
          }
        }
      }
    }
    .login {
      line-height: 24px;
      float: right;
      display: flex;
      align-items: center;
    }
  }
}

.content {
  box-sizing: border-box;
  width: 1024px;
  margin: 0 auto;
  background-color: #f2f2f2;
  padding: 30px 42px 42px 42px;
  .container {
    .top {
      display: flex;
      justify-content: space-between;
      align-items: flex-end;
      margin-bottom: 20px;
      .left {
        font-weight: bold;
        font-size: 24px;
      }
      .right {
        span {
          font-size: 16px;
          color: #9b9b9b;
          margin-right: 20px;
          i {
            color: #000;
            margin: 0 5px;
          }
        }
        select {
          background-color: transparent;
          outline: none;
          border: none;
          font-size: 16px;
          color: #9b9b9b;
        }
      }
    }

    .num {
      display: flex;
      justify-content: space-between;
      margin-bottom: 20px;
      .item {
        box-sizing: border-box;
        width: 300px;
        background-color: #fff;
        box-shadow: 0 0 10px 5px #ebebeb;
        border-radius: 3px;
        padding: 30px;
        .text {
          text-align: center;
          font-size: 16px;
          margin-bottom: 14px;
          i {
            font-size: 26px;
            margin-right: 8px;
          }
        }
        .number {
          font-size: 36px;
          font-weight: bold;
          text-align: center;
        }
        &:nth-child(1) .number {
          color: #7ed321;
        }
        &:nth-child(2) .number {
          color: #d0021b;
        }
        &:nth-child(3) .number {
          color: #4a90e2;
        }
      }
    }

    .line {
      box-shadow: 0 0 10px 5px #ebebeb;
      height: 406px;
      background-image: url(../assets/111.png);
    }

    .product {
      display: flex;
      justify-content: space-between;
      margin-top: 20px;
      .left {
        width: 460px;
        background-color: #fff;
        padding: 30px 40px;
        margin-right: 20px;
        box-sizing: border-box;
        box-shadow: 0 0 10px 5px #ebebeb;
        .title {
          font-weight: bold;
          font-size: 24px;
        }
        .item {
          display: flex;
          align-items: center;
          border-bottom: 1px solid #ebebeb;
          padding: 24px 0;
          i {
            font-size: 45px;
          }
          .icon {
            width: 45px;
          }
          .com {
            margin-left: 20px;
            font-size: 16px;
            color: #9b9b9b;
            width: 120px;
          }
          .count {
            font-size: 20px;
            margin-left: 55px;
            text-align: right;
            width: 56px;
            font-weight: bold;
          }
          .percent {
            font-size: 16px;
            margin-left: 30px;
            font-weight: bold;
            i {
              font-size: 18px;
              margin-right: 5px;
            }
          }
          &:nth-child(2) .percent {
            color: #7ed321;
          }
          &:nth-child(3) .percent {
            color: #7ed321;
          }
          &:nth-child(4) .percent {
            color: #d0021b;
          }
          &:nth-child(5) .percent {
            color: #d0021b;
          }
        }
      }
      .right {
        width: 460px;
        background-color: #fff;
        padding: 30px 40px;
        box-sizing: border-box;
        box-shadow: 0 0 10px 5px #ebebeb;
        .title {
          font-weight: bold;
          font-size: 24px;
          margin-bottom: 22px;
        }
        .item {
          display: flex;
          border-bottom: 1px solid #ebebeb;
          padding: 8px 0;
          .pic {
            width: 100px;
            height: 100px;
            background-color: #069;
          }
          .text {
            margin-left: 21px;
            font-size: 16px;
            color: #9b9b9b;
            .itemName {
              font-weight: bold;
              font-size: 20px;
              margin-top: 11px;
              margin-bottom: 8px;
              color: #000;
            }
            .date {
              margin-bottom: 8px;
              i {
                font-size: 10px;
                margin-right: 8px;
              }
            }
            .name {
              i {
                font-size: 20px;
                margin-right: 13px;
              }
            }
          }
          .total {
            width: 52px;
            margin-left: 60px;
            display: flex;
            flex-direction: column;
            justify-content: flex-end;
            align-items: flex-end;
            margin-bottom: 8px;
            .totalText {
              font-size: 14px;
              margin-bottom: 2px;
            }
            .totalNum {
              font-weight: bold;
              font-size: 20px;
            }
          }
        }
      }
    }
  }
}
</style>
