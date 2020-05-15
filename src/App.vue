
<template>
  <div v-on:click="clickwork" class="circle">
    <span class="counter" :style="{visibility: not_ten ? 'visible' : 'hidden'}" >
      {{ count }} 
    </span> 
  </div>
</template>


<script>
export default {
  data(){
    return{
    count: 0,
    not_ten: false
    }
    },
    methods:{
         clickwork: function () {
            this.count++;
            this.not_ten = true;
        
          if(this.count==10){
            this.count = 0;
            this.not_ten = false;
          }
        }
      }
   
}
</script>


<style>

.circle{
background-color:#e74c3c;
width:300px; 
height:300px; 
border-radius:50%;
text-align: center;
margin-left: 40%;
margin-right: 40%;
margin-top: 15%;  
}

.counter{
color:#fff;
font-size:280px;
}

</style>
