<template>
  <div>
    <div class="div1">
      <h2>LUTÈCE</h2>
      <button class="monb">S'abonner</button>
    </div>

    <div class="menu">
      <ul>
        <li>ACTUALITÉS</li>
        <li>ECONOMIE</li>
        <li>VIDÉOS</li>
        <li>OPINION</li>
      </ul>
    </div>
    <h1>Toute l'actualité</h1>
    <br />
    <br />

    <div class="div3">
      <img class="foot" src="../../assets/img/foot.jpg" alt="" />
      <div class="div3a">Le XV de France s'impose face aux Allblacks</div>
    </div>
    <br />
    <br />
    <br />
    <br />
    <br />
    <div class="article">
      <container-information />
    </div>

    <footer>
      <img class="foot" src="../../assets/img/Footer.png" alt="" />
    </footer>
  </div>
</template>

<script>
</script>

<style scoped>
.div1 {
  display: flex;
  justify-content: space-around;
  margin: 70px;
}
.monb {
  background-color: #505dff;
  border-radius: 50px;
  padding: 5px 10px;
}
.menu ul {
  display: flex;
  justify-content: space-between;
  list-style-type: none;
  margin-left: -30px;
}
h1 {
  padding-left: 2%;
  padding-top: 5%;
  font-size: 30px;
}

.foot {
  width: 100%;
  height: auto;
  top: 0;
}

.div3a {
  background-color: rgb(66, 9, 9, 0.4);
  margin-top: -30px;
  z-index: 3;
  text-align: center;

  /* margin-top: -60px; */
}
/* .article {
  display: flex;
  justify-content: space-between;
} */
.article1 {
  display: flex;
  justify-content: start;
  margin-bottom: 20px;
}
.im {
  width: 150px;
  height: 80px;
  /* background-color: yellow; */
  /* padding-top: 10px; */
  border-radius: 20px;
  /* margin-top: 10px; */
  margin-left: 20px;
}
h3 {
  font-size: 20px;
}
.text {
  margin-left: 10px;
  width: 500px;
  max-width: 100%;
  font-size: 15px;
}
</style>




