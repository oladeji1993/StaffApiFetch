<template>
    <div class="second-one">
        <h1>Question 2. (Fibonacci Series)</h1>
        <input placeholder="Enter a number" v-model= "text" type="text"/>
        <div>
            <button class="btn" @click="getValue()"> Get Fibonacci</button>
            <div :key="item" v-for="item in numbers">
                {{item}}
            </div>
        </div>
    </div>
</template>


<script>

export default {
    name: "Fibonacci",

    data(){
        return{
            text:'',
            numbers : undefined
        }
    },

    methods: {
        getValue(){
            let fibonacci = [0,1];
            var num = this.text;
            for (let i = 1; i < num; i++) {
                fibonacci.push(fibonacci[i] + fibonacci[i - 1]);
            }
            this.numbers = fibonacci
        }
    }
}
</script>


<style scoped>
.btn {
  display: inline-block;
  background: green;
  color: #fff;
  border: none;
  padding: 10px 20px;
  margin: 5px;
  border-radius: 5px;
  cursor: pointer;
  text-decoration: none;
  font-size: 15px;
  font-family: inherit;
}
.btn:focus {
  outline: none;
}
.btn:active {
  transform: scale(0.98);
}

.second-one{
    padding:0px 30px;
}

</style>
