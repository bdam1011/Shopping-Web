<template>
  <div class="content">
    <table style="">
      <thead>
        <tr>
          <th colspan="5">Order</th>
        </tr>
      </thead>
      <tbody>
        <tr class="table-title">
          <td>品項</td>
          <td>數量</td>
          <td>單價</td>
          <td>小計</td>
          <td></td>
        </tr>
        <tr v-for="(product, index) in productsInCart" :key="index">
          <td>{{ product.name }}</td>
          <td>{{ product.amount }}</td>
          <td>{{ product.price }}</td>
          <td>{{ product.sum }}</td>
          <td>
            <button class="button-del" @click="remove(product)">×</button>
          </td>
        </tr>
      </tbody>
      <tfoot>
        <tr>
          <td></td>
          <td colspan="3">
            Total <span class="total-price">$ {{ total }}</span>
          </td>
          <td></td>
        </tr>
      </tfoot>
    </table>
    <button class="checkout">前往付款</button>
  </div>
</template>
<script>
export default {
  data() {
    return {
      productsInCart: [
        {
          name: "地瓜",
          amount: "2",
          price: "50",
          sum: "100",
        },
        {
          name: "地瓜",
          amount: "2",
          price: "50",
          sum: "100",
        },
        {
          name: "地瓜",
          amount: "2",
          price: "50",
          sum: "100",
        },
        {
          name: "地瓜",
          amount: "2",
          price: "50",
          sum: "100",
        },
      ],
    };
  },
  computed:{
    total(){
      var tt=0;
      // var tc=this.productsInCart;      
      for(let i=0;i<2;i++){
        tt=tt+parseInt(this.productsInCart[i].sum);
        
      }
      console.log(tt);
      return tt
    }
  }
};
</script>
<style lang="scss" scoped>
.content {
   justify-content: center; 
    align-items: center; 
}

table {
  margin: 20px;
  width: 100%;
  border-spacing: 0;
  border-collapse: collapse;
  background-color: #fff;
  box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);

  tr {
    border-bottom: 5px solid #f3f3f3;
  }

  th,
  td {
    min-width: 2em;
    width: 15%;
    padding: 15px;
    text-align: right;

    &:first-child {
      width: 40%;
      text-align: left;
    }

    &:last-child {
      padding-right: 10px;
    }
  }

  thead {
    color: #ef8a8b;
    font-size: 16px;
    text-align: left;

    .time {
      color: #c2c2c2;
      font-size: 14px;
      text-align: right;
    }
  }

  tbody {
    font-size: 14px;

    .table-title {
      color: #c2c2c2;
      font-size: 12px;
    }

    .button-del {
      width: 30px;
      height: 30px;
      outline: 0;
      border: 0;
      padding: 0 0 0.4em;
      color: #b6b6b6;
      font-size: 18px;
      background: transparent;
      cursor: pointer;
    }
  }

  tfoot {
    color: #959595;
    font-size: 12px;
    background: #f9f9f9;

    .total-price {
      margin-left: 1em;
      color: #000;
      font-size: 20px;
    }
  }
}

.checkout {
  display: block;
  width: calc(100% - 2 * 20px);
  margin: 20px;
  outline: 0;
  border: 0;
  padding: 15px 0;
  color: #fff;
  font-size: 18px;
  text-align: center;
  background-color: #ef8a8b;
  box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
  cursor: pointer;
}

.icon-container {
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  z-index: 10;
  padding: 30px 20px 0;
  color: #ef8a8b;
  font-size: 20px;
  text-align: center;
  background: rgba(255, 255, 255, 0.8);
  opacity: 0;
  pointer-events: none;
  transition: opacity 0.3s;

  .circle,
  .check {
    fill: none;
    stroke: #ef8a8b;
    stroke-width: 3;
  }

  .check {
    stroke-dasharray: 80 100;
    stroke-dashoffset: 80;
  }

  &.showing {
    opacity: 1;
    pointer-events: auto;

    .check {
      animation: check 0.3s cubic-bezier(0.5, 0, 0.6, 1) forwards 0.2s;
    }
  }
}

@keyframes check {
  from {
    stroke-dashoffset: 80;
  }
  to {
    stroke-dashoffset: 0;
  }
}

@keyframes circle {
  from {
    stroke-dashoffset: -300;
  }
  to {
    stroke-dashoffset: 0;
  }
}
</style>