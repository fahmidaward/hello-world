<template>
    <div  id="app" class="add">
        <h3>Search the position of a substing within a string</h3>
        <form id="sum">
         <fieldset>
            <label for="">TEXT: </label>
            <input type="text" class="form-control" v-model="num1">
         </fieldset>
         <fieldset>
            <label for="">SubTEXT: </label>
            <input type="text" class="form-control" v-model="num2">
         </fieldset>
            <button @click="addNumbers" type="button" class="btn btn-light">
                Click me!
            </button>
        </form>
        <p><strong>Position:</strong> {{ sum }}</p>
    </div>
</template>
<script>
export default {
  name: 'Add',
  data() {
    return {
      num1: 0,
      num2: 0,
      sum: 0,
    };
  },
  methods: {
    addNumbers() {
      this.sum = this.num1.toLowerCase().indexOf(this.num2.toLowerCase());
    },
  },
};
</script>
<style scoped>
    .add {
        background: #d67182;
        box-shadow: 1px 3px 6px #a3a3a3;
        padding: 50px 30px;
        width: 350px;
        text-align: center;
        margin: 80px auto;
    }
    p, h3 {
        color: #FFFFFF;
    }
    #sum {
        margin-top: 25px;
    }
    .form-control {
        margin-bottom: 15px;
    }
    .btn {
        margin-bottom: 30px;
    }
</style>
