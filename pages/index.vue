<template>
  <div class="main">
    <nav-component-white />
    <img src="../assets/img/deux-amis-passent-le-temps-en-parc-modèles-d-enfants-134334706.png" alt="img top"
      class="img1">
    <div class="align">
      <div class="logoLeft">
        <div>
          <img src="../assets/img/Groupe 28.png" alt="img health">
          <h2>Health</h2>
        </div>
        <div>
          <img src="../assets/img/932c7ee0a32644e2a25da904f777be7a.png" alt="img clock">
          <h2>Clock</h2>
        </div>
        <div>
          <img src="../assets/img/Groupe 27.png" alt="img camera">
          <h2>Caméra</h2>
        </div>
        <div>
          <img src="../assets/img/Groupe 26.png" alt="img horloge">
          <h2>Snapchat</h2>
        </div>
        <div>
          <img src="../assets/img/1200px-Instagram_logo_2016.png" alt="logo insta">
          <h2>Instagram</h2>
        </div>
      </div>
      <div class="right">
        <img src="../assets/img/Composant 5 – 1.png" alt="img son">
        <h2>Music</h2>
      </div>
    </div>
    <div class="bottom">
      <img src="../assets/img/Groupe 30.png" alt="img screen" class="screen">
      <div class="favoris">
        <img src="../assets/img/Composant 9 – 1.png" alt="tel">
        <NuxtLink :to="'/informations'">
        <img src="../assets/img/Composant 8 – 1.png" alt="safari" class="spe">
        </NuxtLink>
        <NuxtLink :to="'/messages'">
        <img src="../assets/img/Composant 7 – 1.png" alt="message" class="spe">
        </NuxtLink>
        <img src="../assets/img/Composant 6 – 1.png" alt="son">
      </div>
    </div>
  </div>

</template>

<script>

</script>

<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Roboto&display=swap');
  *{
    font-family: Roboto;
  }
  .screen{
    display: flex;
    margin: 10px auto;
  }
  .favoris{
    display: flex;
    width: 95%;
    padding: 20px;
    border-radius: 30px;
    background-color: #ECECEC;
    margin: 0 auto;
    align-items: end;
    justify-content: space-between;
  }
  .main {
    height: 100vh;
    width: 100%;
    background-image: url("../assets/img/e254584474c0872999b1fd2beaf70a19.png");
    background-position: center;
    background-repeat: no-repeat;
    background-size: 100% 100vh;
  }
  .favoris img {
    width: 80px;
    height: 80px;
  }
  .spe{
    width: 85px !important;
    height: 85px !important;
  }

  .img1 {
    width: 354px;
    height: 172px;
    margin: 20px auto;
    display: flex;
  }

  .logoLeft img {
    width: 80px;
    height: 80px;
  }

  h2 {
    font-size: 14px;
    color: white;
    margin-top: 5px;
    text-align: center;
  }

  .logoLeft div {
    width: fit-content;
  }
  .logoLeft{
    width: 50%;
    display: flex;
    flex-wrap: wrap;
    justify-content: space-between;
  }
  .align{
    display: flex;
    width: 83%;
    margin: 0 auto;
    justify-content: space-between;
  }
  .bottom{
    margin-top: 180px;
  }

</style>
