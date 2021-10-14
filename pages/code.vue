<template>
  <div class="code">
    <nav-component-white/>
    <div class="infos">
      <img src="../assets/img/Icon awesome-lock.png" alt="lock">
      <h2>{{heure}}</h2>
      <p>{{date}}</p>
    </div>
    <div class="container">
      <p>Saisissez le code</p>
      <div v-if="nbr == 0" class="containCircle">
        <div class="circle"></div>
        <div class="circle"></div>
        <div class="circle"></div>
        <div class="circle"></div>
      </div>
      <div v-if="nbr == 1" class="containCircle">
        <div class="circleFull"></div>
        <div class="circle"></div>
        <div class="circle"></div>
        <div class="circle"></div>
      </div>
      <div v-if="nbr == 2" class="containCircle">
        <div class="circleFull"></div>
        <div class="circleFull"></div>
        <div class="circle"></div>
        <div class="circle"></div>
      </div>
      <div v-if="nbr == 3" class="containCircle">
        <div class="circleFull"></div>
        <div class="circleFull"></div>
        <div class="circleFull"></div>
        <div class="circle"></div>
      </div>
      <div class="chiffres">
        <p @click="add(1)">1</p>
        <p @click="add(2)">2</p>
        <p @click="add(3)">3</p>
        <p @click="add(4)">4</p>
        <p @click="add(5)">5</p>
        <p @click="add(6)">6</p>
        <p @click="add(7)">7</p>
        <p @click="add(8)">8</p>
        <p @click="add(9)">9</p>
        <p @click="add(0)">0</p>
      </div>
    </div>
  </div>
</template>

<script>
  export default {
    data() {
      return {
        heure: '',
        date: '',
        nbr: 0,
        result: '',
        chiffre: '7124',
      }
    },

    mounted() {
      var date = new Date()
      var minutes = date.getMinutes()
      var hour = date.getHours()
      var jour = date.getDate()
      let months = ["Janvier", "Février", "Mars", "Avril", "Mai", "Juin", "Juillet", "Aout", "Septembre", "Octobre", "Novembre", "Decembre"]
      var month = months[date.getMonth()]
      var actualYear = date.getFullYear();

      if(jour <10){
        this.date = "0" + jour + ' ' + month + ' ' + actualYear
      }else{
        this.date = jour + ' ' + month + ' ' + actualYear
      }

      if (minutes < 10) {
        this.heure = hour + ':' + '0' + minutes
      } else {
        this.heure = hour + ':' + minutes
      }
    },

    methods: {
      add(chiffre){
        console.log(chiffre);
        this.nbr += 1
        this.result = this.result + chiffre
        console.log(this.result);
        if(this.nbr == 4){
          console.log("dans la verif");
        }
      }
    },
  }
</script>

<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Roboto&display=swap');
  *{
    font-family: Roboto;
  }
  .code{
    height: 100vh;
    width: 100%;
    background-image: url("../assets/img/BG.jpg");
    background-position: center;
    background-repeat: no-repeat;
    background-size: 75vh 105vh;
  }
  img{
    width: 31px;
    height: 36px;
  }
  h2{
    color: white;
    font-size: 70px;
    font-weight: 300;
  }
  .infos p {
    font-size: 23px;
    color: white;
  }
  .infos{
    text-align: center;
    padding-top: 55px;
  }
  .container{
    text-align: center;
    color: white;
  }
  .container p {
    font-size: 23px;
  }
  .chiffres p{
    font-size: 32px;
    padding: 15px 30px;
    border-radius: 40px;
    background-color: #707070;
    margin: 20px;
    opacity: 0.8;
    cursor: pointer;
  }
  .chiffres {
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
    width: 90%;
    margin: 10px auto;
  }
  .circle{
    width: 18px;
    height: 18px;
    border: solid 2px #FFFFFF;
    border-radius: 40px;
  }
  .circleFull{
    width: 18px;
    height: 18px;
    border: solid 2px #FFFFFF;
    border-radius: 40px;
    background-color: white;
  }
  .containCircle{
    display: flex;
    width: 30%;
    margin: 10px auto;
    justify-content: space-between;
  }
</style>

