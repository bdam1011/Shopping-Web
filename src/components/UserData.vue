<template>
<div class="aawe">
  <div>
    <img src="https://d1grca2t3zpuug.cloudfront.net/2019/05/ajisai20.jpg" />
  </div>
  <br>
  <div>
    <ul class="userInfo">
      <li>Userid: {{info.Userid}}</li>
      <li>Name: {{info.Name}}</li>
      <li>Nickname: {{info.Nickname}}</li>
      <li>Gender: {{info.Gender}}</li>
      <li>Birthday: {{info.Birthday}}</li>
      <li>Phone: {{info.Phone}}</li>
      <li>Address: {{info.Address}}</li>
      <li>Email: {{info.Email}}</li>
      <li>CreditCards: {{info.CreditCards}}</li>
    </ul>
  </div>
</div>
</template>

<script>
export default {
  name: "UserData",
  data() {
    return {
      info: {
        Userid: "ONE",
        Name: "haha",
        Nickname: "hihi",
        Gender: "male",
        Birthday: "1999/9/9",
        Phone: "0999999999",
        Address: "Taichung",
        Email: "ONE@gmail.com",
        CreditCards: "1321354546563",
      },
    };
  },
};
</script>
<style scoped>
.aawe{
    left: 0px;
    justify-content: center; 
    align-items: center; 
    width: 20vw;
    padding:20px;
}
img{
   
    left: 0px;
    width: 100%;

}
.userInfo{
    list-style-position: inside;
    text-align: left;
    border: solid;
    width: 100%;
    margin: 0px;
    padding:0px;
}
</style>