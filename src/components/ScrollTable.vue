<template>
  <div>
    <table>
      <thead>
          <tr>
              <td colspan="4">{{title}}</td>
              <td><button>{{tittleButton}}</button></td>
          </tr>
        <tr>
          <th v-for="(thead, key, index) in theads" :key="index">
            {{ thead }}
          </th>
          <th>操作</th>
        </tr>
      </thead>
      <tbody>
        <tr v-for="(tbody,index) in tbodys" :key="tbody.id">
          <td v-if="!tbody.show">{{ tbody.id }}</td>
          <td v-if="tbody.show"><input type="text" v-model="tbodys[index].id"></td>
          <td v-if="!tbody.show">{{ tbody.name }}</td>
          <td v-if="tbody.show"><input type="text" v-model="tbodys[index].name"></td>
          <td v-if="!tbody.show">{{ tbody.price }}</td>
          <td v-if="tbody.show"><input type="text" v-model="tbodys[index].price"></td>
          <td v-if="!tbody.show">{{ tbody.storages }}</td>
          <td v-if="tbody.show"><input type="text" v-model="tbodys[index].storages"></td>
          <td><button :id="index" @click="show()">修改/儲存</button></td>
        </tr>
      </tbody>
      
      <tfoot>
          <tr>
            <td colspan="5"><button>{{tfoot}}</button></td>
          </tr>
      </tfoot>
    </table><br>
    {{tbodys[0].id}}{{tbodys[0].name}}{{tbodys[0].price}}
  </div>
</template>
<script>
export default {
  name: "ScrollTable",
  methods:{
    show(){
      if(this.tbodys[event.srcElement.id].show){
        this.tbodys[event.srcElement.id].show=false;
      }else{
        this.tbodys[event.srcElement.id].show=true;
      }
     
    }
  },
  data() {
    return {
        title:"商品庫存",
        tittleButton:"商品新增",
        tfoot:"商品移除",
      theads: ["ID", "Name", "Price(NT)", "Storages"],
      tbodys: [
        {
          id: "3",
          name: "food",
          price: "400",
          storages: "4",
          show:false
        },
        {
          id: "123",
          name: "food",
          price: "400",
          storages: "4",
          show:false
        },
        {
          id: "123",
          name: "food",
          price: "400",
          storages: "4",
          show:false
        },
        {
          id: "123",
          name: "food",
          price: "400",
          storages: "4",
          show:false
        },
        {
          id: "123",
          name: "food",
          price: "400",
          storages: "4",
          show:false
        },
        {
          id: "123",
          name: "food",
          price: "400",
          storages: "4",
          show:false
        },
        {
          id: "123",
          name: "food",
          price: "400",
          storages: "4",
          show:false
        },

      ],
    };
  },
};
</script>
<style scoped>
div {
  border-style: solid;
  overflow-x: auto;
  overflow-y: auto;
  /* right: 0px;
  justify-content: center;
  align-items: center;
  width: 80vw;
  padding: 10px; */
}
table {
  border-collapse: collapse;
  border-spacing: 0;
  width: 100%;
  border: 1px solid #ddd;
}
th,tbody{
    border-style: solid;
}

th,
td {
  text-align: center;
  padding: 8px;
}
tr:nth-child(even){background-color: #f2f2f2}
</style>