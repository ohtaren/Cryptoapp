<template>
  <div id="detail">
    <div class="header-flex">
     <p class="left">Cryptoapp</p>
     <nav class="right">
       <p><a @click="$router.push({ name: 'Home' })">ホームに戻る</a></p>
       <p><a @click="$router.push({ name: 'Login' })">ログアウト</a></p>
     </nav>
   </div>
   <div class="detail-card">
     <p class="card-title">【通貨詳細】</p>
     <table class="data">
          <tr class="data-title">
            <th>Value</th>
            <th>Description</th>
            <th>Price</th>
            <th>Release date</th>
          </tr>
          <tr>
            <td>{{coin}}</td>
            <td>ビットコイン（現物取引）</td>
            <td>¥{{symbol}}</td>
            <td>2018/09/05</td>
          </tr>      
     </table>
   </div>
  </div>
</template>

<script>
import axios from "axios";

export default {
  props:["coin"],
  data(){
    return{
      price:""
    };
  },
  async created(){
    const symbol = await axios.get(
      `https://api.coin.z.com/public/v1/ticker?symbol=${this.coin}`
    );
    console.log(symbol)
    this.price = symbol,[0]
  }
};

</script>


<style scoped>
#detail{
  background-image: url("../assets/background3.jpg");
  background-size: cover;
  width: 100vw;
  height: 100vh;
}

.header-flex{
  background-color: black;
  width: 100vw;
  height: 38px;
}

.left{
  color: white;
  font-size: 22px;
  position: absolute;
  top: 8px;
  left: 10px;
}

.right{
  display: flex;
  position: absolute;
  top: 15px;
  right: 30px;
  font-size: 13px;
  list-style: none;
}

.right p{
  color: white;
}

.right a{
  margin-left: 20px;
  cursor: pointer;
  text-decoration: underline;
}

.detail-card{
  background-color:#ffffff;
  width: 70%;
  height: 50%;
  position: relative;
  top: 20%;
  left: 15%;
}

.card-title{
  position: relative;
  top: 30px;
  left: 25px;
  font-size: 13px;
}

.data {
 width: 65vw;
 margin-top: 40px;
 margin-left: 20px;
 justify-content: center;
 text-align: center;
}

.deta-title{
  margin-bottom: 20px;
  text-decoration: underline;
  text-decoration-color: black;
}

table{
   font-size: 13px;
}

</style>