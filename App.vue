<template>
  <div>
    <input type="text" v-model="text">
    <button  @click="handadd">提交</button>
    <ul >
      <li 
      v-for="(item, index) in list"
      :key="index"
      @click="removeItem(index)"
      >
       {{index+1}} .{{item}}
      </li>
    </ul>
  </div>
</template>

<script>
  export default {
    data() {
      return({
        list: [
         
        ],
        text: ''
      })
    },
    methods: {
      handadd() {
        this.list.push(this.text)
        this.text = ''
      },
      removeItem(index){
        this.list.splice(index, 1)
      }
    }
  }
</script>

<style>

</style>
