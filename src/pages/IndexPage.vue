<template>
  <q-page class="flex flex-center">
<q-btn class="main_btn" v-model="expense" @click="expense_click">Expense</q-btn>
<q-btn class="main_btn" v-model="income" @click="income_click">Income</q-btn>
<!-- <q-separator/><br/> -->
<q-input outlined class="input_amt" v-model="amount" aria-placeholder="Amount"/>
<q-btn class="main_btn" v-model="add" @click="add">Add</q-btn>

<div class="display">


</div>
  </q-page>
</template>

<script>
import { defineComponent } from 'vue'

export default defineComponent({
  name: 'IndexPage',
  expense: false,
  income: false,
  amount:0,
  list_amt:[],
  methods:{
    expense_click() {
      this.expense=true;
      this.income= false;
    },
    income_click() {
      this.expense=false;
      this.income= true;
    }
  }
})
</script>
<style>
.input_amt{
margin: 50px;
background-color: rgb(230, 223, 223);
color:black;
font-size:1.5rem;
}
.main_btn{
  font-size: 1.5rem;
  margin: 10px;
  background-color: rgb(138, 138, 200);
}
.display{

}
.q-field__control {
    color: red;
    height: 56px;
    max-width: 100%;
    outline: none;
}
</style>