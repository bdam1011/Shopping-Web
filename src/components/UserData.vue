<template>
  <div class="user">
    <div class="userhead" v-bind:style="{'background-image':picture}"></div>
    <br />
    <div>
      <table class="userInfo">
        <tr>
          <th>User Information</th>
        </tr>
        <tr>
          Userid: {{info.Userid}}
        </tr>
        <tr>
          Name: {{info.Name}}
        </tr>
        <tr>
          Nickname: {{info.Nickname}}
        </tr>
        <tr>
          Gender: {{info.Gender}}
        </tr>
        <tr>
          Birthday: {{info.Birthday}}
        </tr>
        <tr>
          Phone: {{info.Phone}}
        </tr>
        <tr>
          Address: {{info.Address}}
        </tr>
        <tr>
          Email: {{info.Email}}
        </tr>
        <tr>
          CreditCards: {{info.CreditCards}}
        </tr>
      </table>
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
      url: "https://d1grca2t3zpuug.cloudfront.net/2019/05/ajisai20.jpg"
    };
  },
  computed:{
    picture(){
      return "url("+this.url+")"
    }
  },
};
</script>
<style scoped>
.user {
  left: 0px;
  justify-content: center;
  align-items: center;
  width: 20vw;
  padding: 20px;
}
.userhead {
  width: 20vw;
  height: 20vw;
  border-radius: 50%;
  /* background-image: url("https://d1grca2t3zpuug.cloudfront.net/2019/05/ajisai20.jpg"); */
  background-size: 200%;
  background-repeat: no-repeat;
  background-position: 50% 0;
}

.userInfo {
  border: solid;
  width: 100%;
  margin: 0px;
  padding: 0px;
  text-align: left;
}
.userInfo tr {
  height: 1.5rem;
}
tr:first-child {
  color: #fff;
  background-color: #00ced1;
}
</style>