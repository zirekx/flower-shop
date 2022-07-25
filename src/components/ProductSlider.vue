<template>
  <div id="Slider">
    <div class="left">
     <svg  v-bind:style="{transform: `rotate(${deg}deg)`}" id="visual" viewBox="0 0 900 600" width="100%" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" version="1.1">
        <g :style="{fill:color}" transform="translate(-25.925599898795326 36.01359749837587)"><path d="M272.7 -457.9C355.7 -370.9 427.1 -299.3 483.8 -210.5C540.5 -121.8 582.5 -16 588.3 98.9C594 213.8 563.4 337.7 482 400C400.6 462.3 268.3 462.8 147.6 494.6C26.9 526.4 -82.4 589.4 -164.1 563.4C-245.8 537.3 -300 422.1 -350.3 325.2C-400.5 228.3 -446.7 149.6 -486.2 53.4C-525.7 -42.8 -558.5 -156.4 -519.8 -235.8C-481 -315.2 -370.8 -360.3 -272.3 -440.3C-173.7 -520.3 -86.9 -635.2 4 -641.3C94.8 -647.5 189.6 -545 272.7 -457.9" ></path></g>
      <text x="20%" y="50%" fill="white">
        {{this.slide[i].name}}
      </text>></svg>
    
    </div>
    
    <button @click="animate">Animacja </button>
  </div>
</template>

<script>
export default {
  name: 'ProductSlider',
  data(){
    return {
      deg: 0,
      color:'red',
      i:0,
      slide: [
        {
          bgcolor:'yellow',
          name:'Róża1',
          length:'27',
          color: 'examplecolor',
          material:'examplematerial'
          
          
        },
        {
          bgcolor:'green',
          name:'Róża2',
          length:'27',
          color: 'examplecolor',
          material:'examplematerial'
        },
        {
          bgcolor:'violet',
          name:'Róża3',
          length:'27',
          color: 'examplecolor',
          material:'examplematerial'
        },
        {
          bgcolor:'red',
          name:'Róża4',
          length:'27',
          color: 'examplecolor',
          material:'examplematerial'
        }

      ]
    }
  },
  methods:{
    animate(){
       this.deg += 20;
      
      this.color=this.slide[this.i].bgcolor;
      this.i++;
      if(this.i>3){
        this.i=0;
      }
    },
    rotation(){
           

    }
  },
  mounted() {
   
  },
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
$primary-color:#2cbc63;
$background:#666666;
#Slider{
  height:620px;
  width:100%;
  background-color:$background;
  color:black;
  margin:0;
}
.left{
  float:left;
  width:70%;
}
svg{
  
  
}
</style>
