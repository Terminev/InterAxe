<template>
  <div class="align">
    <div class="left">
      <h2>{{heure}}</h2>
    </div>
    <div class="right">
      <img src="../assets/img/Réseau.png" alt="img reseau" class="img1">
      <img src="../assets/img/4G.png" alt="img 4g" class="img2">
      <img src="../assets/img/Batterie.png" alt="img batterie" class="img3">
    </div>
  </div>
</template>

<script>
  export default {
    data() {
      return {
        heure: '',
      }
    },

    mounted() {
      var date = new Date()
      var minutes = date.getMinutes();
      var hour = date.getHours();
      if (minutes < 10) {
        this.heure = hour + ':' + '0' + minutes
      } else {
        this.heure = hour + ':' + minutes
      }
    },

    methods: {

    },
  }

</script>

<style scoped>
  .align {
    padding-top: 18px;
    margin: 0 auto;
    display: flex;
    justify-content: space-between;
    width: 90%;
  }

  .right {
    display: flex;
    align-items: center;
    width: 18%;
    justify-content: space-between;
  }

  .img1 {
    width: 18px;
    height: 14px;
  }

  .img2 {
    width: 17px;
    height: 17px;
  }

  .img3 {
    width: 23px;
    height: 11px;
  }

  h2 {
    font-size: 20px;
  }

</style>
