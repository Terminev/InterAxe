<template>
  <div class="code">
    <nav-component-white />
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
    <div class="error" id="error">
      <div class="errorMessage">
        <img src="../assets/img/cancel.png" alt="cross" class="close" @click="closeError()">
        <h2>Le code est incorrect !</h2>
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
      let months = ["Janvier", "Février", "Mars", "Avril", "Mai", "Juin", "Juillet", "Aout", "Septembre", "Octobre",
        "Novembre", "Decembre"
      ]
      var month = months[date.getMonth()]
      var actualYear = date.getFullYear();

      if (jour < 10) {
        this.date = "0" + jour + ' ' + month + ' ' + actualYear
      } else {
        this.date = jour + ' ' + month + ' ' + actualYear
      }

      if (minutes < 10) {
        this.heure = hour + ':' + '0' + minutes
      } else {
        this.heure = hour + ':' + minutes
      }
    },

    methods: {
      add(chiffre) {
        console.log(chiffre);
        this.nbr += 1
        this.result = this.result + chiffre
        console.log(this.result);
        if (this.nbr == 4) {
          if (this.result == this.chiffre) {
            console.log(this.result);
            console.log(this.chiffre);
            window.location.href = '/'
          } else {
            this.nbr = 0
            this.result = ''
            var error = document.getElementById("error")
            error.style.display = "flex"
          }
        }
      },
      closeError(){
        var error = document.getElementById("error")
        error.style.display = "none"
      }
    },
  }

</script>

<style scoped>
  @import url('https://fonts.googleapis.com/css2?family=Roboto&display=swap');

  * {
    font-family: Roboto;
  }

  .code {
    position: relative;
    height: 100vh;
    width: 100%;
    background-image: url("../assets/img/BG.jpg");
    background-position: center;
    background-repeat: no-repeat;
    background-size: 75vh 105vh;
  }

  img {
    width: 31px;
    height: 36px;
  }

  .close {
    width: 40px;
    height: 40px;
    position: absolute;
    top: 395px;
    right: 52px;
  }

  h2 {
    color: white;
    font-size: 70px;
    font-weight: 300;
  }

  .error {
    position: absolute;
    width: 100%;
    height: 100vh;
    top: 0;
    background-color: rgba(0, 0, 0, 0.65);
    display: none;
  }

  .errorMessage {
    padding: 30px 20px;
    border-radius: 20px;
    background-color: rgb(187, 187, 187);
    width: 80%;
    margin: auto;
    display: flex;
  }

  .errorMessage h2 {
    font-size: 35px !important;
    text-align: center;
  }

  .infos p {
    font-size: 23px;
    color: white;
  }

  .infos {
    text-align: center;
    padding-top: 55px;
  }

  .container {
    text-align: center;
    color: white;
  }

  .container p {
    font-size: 23px;
  }

  .chiffres p {
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

  .circle {
    width: 18px;
    height: 18px;
    border: solid 2px #FFFFFF;
    border-radius: 40px;
  }

  .circleFull {
    width: 18px;
    height: 18px;
    border: solid 2px #FFFFFF;
    border-radius: 40px;
    background-color: white;
  }

  .containCircle {
    display: flex;
    width: 30%;
    margin: 10px auto;
    justify-content: space-between;
  }

</style>
