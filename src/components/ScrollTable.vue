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
        <tr v-for="tbody in tbodys" :key="tbody.id">
          <td>{{ tbody.id }}</td>
          <td>{{ tbody.name }}</td>
          <td>{{ tbody.price }}</td>
          <td>{{ tbody.storages }}</td>
          <td><button>修改/儲存</button></td>
        </tr>
      </tbody>
      <tfoot>
          <tr>
            <td colspan="5"><button>{{tfoot}}</button></td>
          </tr>
      </tfoot>
    </table>
  </div>
</template>
<script>
export default {
  name: "ScrollTable",
  data() {
    return {
        title:"商品庫存",
        tittleButton:"商品新增",
        tfoot:"商品移除",
      theads: ["ID", "Name", "Price(NT)", "Storages"],
      tbodys: [
        {
          id: "123",
          name: "food",
          price: "400",
          storages: "4",
        },
        {
          id: "123",
          name: "food",
          price: "400",
          storages: "4",
        },
        {
          id: "123",
          name: "food",
          price: "400",
          storages: "4",
        },
        {
          id: "123",
          name: "food",
          price: "400",
          storages: "4",
        },
        {
          id: "123",
          name: "food",
          price: "400",
          storages: "4",
        },
        {
          id: "123",
          name: "food",
          price: "400",
          storages: "4",
        },
        {
          id: "123",
          name: "food",
          price: "400",
          storages: "4",
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