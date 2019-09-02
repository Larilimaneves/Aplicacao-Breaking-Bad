<template>
 <nav>
  <img src="./assets/breaking.png">
  <button class=""> 
  </button>
  <input placeholder='Pesquise os personagens' type="search">

  <h2>Personagens</h2>

  <div class="characters">
       <div class = " character-map">
      <img v:bind:id= ""class ='char-img' v-bind:src="characters" alt="">
      <img class ='char-img' v-bind:src="characters" alt="">

</div>

  <div class = " character-map">
      <img class ='char-img' v-bind:src="characters" alt="">
      <img class ='char-img' v-bind:src="characters" alt="">

</div>

  <div class = " character-map">
      <img class ='char-img' v-bind:src="characters" alt="">
      <img class ='char-img' v-bind:src="characters" alt="">

</div>
  <div class = " character-map">
      <img class ='char-img' v-bind:src="characters" alt="">
      <img class ='char-img' v-bind:src="characters" alt="">

</div>
</div>
             
 </nav>
 
</template>

<script>

    var axios = require('axios');

   axios.get("https://breakingbadapi.com/api/characters").then (function(resposta){
    console.log(resposta.data);
})



/*export default{
    name:'characters',
    props:{
      id:{
        type: Integer
      },
      name:{
        type:String
      },
    birthday: {
      type: String
    },
    occupationarray:{
      type:Array
    },
    img:{
      type:String
    },
    nicknamestring:{
      type:String
    },
    
    portrayedstring:{
      type:String
    },

    }
}*/

</script>

<style>
img{
  width: 250px;
  margin-left:50px;
 
}
nav{
  height: 700px;
  background-color: black;
}
input{
  height: 25px;
  width: 20%;
  margin-top:40px;
  float: right;
  border-block-start: 10pt ;
  font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
  font-size: 15px;
  padding-block-end: 10px;
  background-color:black;
  
}

button{
  margin-top: 40px;
  height:25px;
  width: 30px;
  float: right;
  margin-right:150px;
  background: black;
  border-radius: 100%

}
h2{
  color: white;
  font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
  margin-left: 100px;
  margin-top:10px;
  background-color:black;
  flex-wrap: wrap;
 
}
.characters{
 display: flex;
 align-items: center;
 justify-content:space-around;


}
.character-map{
  background-color: black;
  justify-content:space-around;
  flex-wrap: wrap;
  display: flex;
  align-items: center;
}



.char-img{
  width: 220px;
  height: 280px;
  margin:10px;
  margin-top: 20px;
 
}
</style>