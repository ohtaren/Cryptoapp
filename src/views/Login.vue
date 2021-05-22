<template>
 <div id="login">
   <div class="login-card">
     <p class="card-title">Cryptoapp</p>
     <p class="page-title">ログイン</p>
     <div class="form">
       <div class="e-mail">
        <p>メールアドレス</p>
        <input type="email">
       </div>
       <div class="password">
         <p>パスワード ※8文字以上</p>
         <input type="password">
       </div>
       <button  @click="$router.push({ name: 'Home' })">ログイン</button>
       <nav class="page-change">初めての方は<a  @click="$router.push({ name: 'Register' })">こちら</a></nav>
     </div>
   </div>
 </div>
</template>

<style scoped>
#login{
  background-image:url("../assets/background2.jpg");
  background-size: cover;
  width: 100vw;
  height: 100vh;
}

.login-card{
  width: 34%;
  height: 65%;
  background-color: #ffffff;
  padding: 20px;
  position: relative;
  top: 15%;
  left: 33%;
}

.card-title{
  color: black;
  font-size: 20px;
  font-weight: bold;
  text-align: center;
  margin-top: 5px;
}

.page-title{
  color: black;
  font-size: 15px;
  text-align: center;
  margin-top: 20px;
}

.form p{
  color: black;
  font-size: 10px;
  margin-top: 16px;
  margin-bottom: 5px;
  position: relative;
  left: 20%;
}

.form input{
  position: relative;
  left: 20%;
  color: black;
  font-size: 12px;
}

.form button{
 position: relative;
 left: 40%;
 margin-top: 10px;
 font-size: 10px;
 padding: 2px 8px;
 background-color:#B9DAF9;
 border-radius: 20px;
 cursor: pointer;
}

.page-change{
  text-align:center;
  font-size: 10px;
  color:black;
  margin-top: 12px;
}

.page-change a{
  color: #B9DAF9;
  cursor: pointer;
  text-decoration:underline ;
}
</style>