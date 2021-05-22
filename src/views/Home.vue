<template>
 <div id="home">
   <div class="header-flex">
     <p class="left">Cryptoapp</p>
     <nav class="right"><a @click="$router.push({ name:'Login'})">ログアウト</a></nav>
   </div>
   <div class="home-card">
     <p class="card-title">【通貨一覧】</p>
     <table class="datalist">
          <tr class="data-title">
            <th>Value</th>
            <th>Description</th>
            <th>Release date</th>
            <th>Detail</th>
          </tr>
           <tr>
              <td>BTC</td>
              <td>ビットコイン（現物取引）</td>
              <td>2018/09/05</td>
              <td><button @click="$router.push({name:'Detail', params:{coin:'BTC'}})">詳細</button></td>
           </tr>
           <tr>
              <td>ETH</td>
              <td>イーサリアム（現物取引）</td>
              <td>2018/09/05</td>
              <td><button @click="$router.push({name:'Detail', params:{coin:'ETH'}})">詳細</button></td>
            </tr>          
            <tr>
              <td>BCH</td>
              <td>ビットコインキャッシュ（現物取引）</td>
              <td>2018/09/05</td>
              <td><button @click="$router.push({name:'Detail', params:{coin:'BCH'}})">詳細</button></td>
            </tr>
            <tr>
              <td>LTC</td>
              <td>ライトコイン（現物取引）</td>
              <td>2018/09/05</td>
              <td> <button @click="$router.push({name:'Detail', params:{coin:'LTC'}})">詳細</button></td>
            </tr>          
            <tr>
              <td>XRP</td>
              <td>リップル（現物取引）</td>
              <td>2018/09/05</td>
              <td> <button @click="$router.push({name:'Detail', params:{coin:'XRP'}})">詳細</button></td>
            </tr>
     </table>
   </div>
 </div>
</template>

<script>

export default {
  name: 'Home',
};
</script>

<style scoped>
#home{
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
  font-size: 22px;
  color: white;
  position: absolute;
  top: 8px;
  left: 10px;
}

.right{
  position: absolute;
  top: 15px;
  right: 30px;
  font-size: 13px;
}

.right a{
  color: white;
  cursor: pointer;
  text-decoration: underline;
}

.home-card{
  background-color:#ffffff;
  width: 75%;
  height: 65%;
  position: relative;
  top: 12%;
  left: 15%;
}

.card-title{
  position: relative;
  top: 25px;
  left: 30px;
  font-size: 13px;
}

.datalist{
  width: 65vw;
  margin-top: 40px;
  margin-left: 30px;
  justify-content: center;
  text-align: center;
}

.deta-title{
  text-decoration-line: underline;
  text-decoration-color: black;
}

table {
  font-size: 12px;
}

button{
  background-color: #B9DAF9;
  padding: 2px 8px;
  border-radius: 20px;
  cursor: pointer;
  margin-top: 3px;
}
</style>
