<template>
  <div>
    <img src="https://i1.kknews.cc/NvxRvur4qlHQ5xXxcRBZqOmGWYxBE3n666CG2kQ/0.jpg" />
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
img{
    position: fixed;
    left: 0px;

}
.userInfo li{
    list-style-position: inside;
    text-align: left;
    border: solid;
    width: 20vw;
}
</style>