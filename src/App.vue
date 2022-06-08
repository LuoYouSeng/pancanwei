<script>
import { defineComponent } from "vue"

export default defineComponent({
    data(){
      return {
          opacity: 0
      }  
    },
    methods: {
        bianhong(){
            this.opacity += 0.05
        }
    },
    computed: {
        compute(){
            return {
                'background-color': 'rgba(255,0,0,'+this.opacity+')'
            }
        }
    }
})
</script>

<template>
  <h1>吴培炜好帅</h1>
  <img src="./assets/a.jpg">
  <div class="piar">
      <div class="lian" :style="compute"></div>
      <div class="lian" :style="compute"></div>
  </div>
  <button @click="bianhong()">点我</button>
  <h1>啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊</h1>
</template>

<style>
.piar{
    transform: translateY(-5rem) translateX(3rem);
    display: flex;
}
.lian{
    width: 2.5rem;
    height: 1.5rem;
    background-color: rgba;
    border-radius: 100%;
}
.lian:nth-child(2){
    transform: translateX(1rem);
}
</style>
