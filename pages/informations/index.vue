<template>
  <div>
    <div class="div1">
      <div class="burgerb">
        <span></span>
        <span></span>
      </div>
      <h2>LUTÈCE</h2>
      <button class="monb">S'abonner</button>
    </div>

    <div class="menu">
      <ul>
        <li>ACTUALITÉS <i class="arrow down"></i></li>
        <li>ECONOMIE <i class="arrow down"></i></li>
        <li>VIDÉOS <i class="arrow down"></i></li>
        <li>OPINION <i class="arrow down"></i></li>
      </ul>
    </div>
    <h1>Toute l'actualité</h1>

    <div class="div3">
      <img class="foot" src="../../assets/img/foot.jpg" alt="" />
      <div class="div3a">Le XV de France s'impose face aux Allblacks</div>
    </div>

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
.burgerb span {
  width: 50px;
  height: 2px;
  background-color: black;
}
.div1 {
  display: flex;
  justify-content: space-around;
  background-color: #f9f9f9;
  padding: 15px 5px;
  margin-bottom: 20px;
}
.monb {
  background-color: #505dff;
  border-radius: 50px;
  padding: 5px 10px;
  color: white;
  border-style: none;
}
.menu ul {
  display: flex;
  justify-content: space-between;
  list-style-type: none;
  margin-left: -30px;
}
.arrow {
  border: solid black;
  border-width: 0 3px 3px 0;
  display: inline-block;
  padding: 5px;
  margin-bottom: 2px;
  margin-left: 2px;
}
.down {
  transform: rotate(45deg);
  -webkit-transform: rotate(45deg);
}
h1 {
  padding-left: 2%;
  padding-top: 5%;
  font-size: 30px;
  margin-bottom: 30px;
}

.foot {
  width: 100%;
  height: auto;
  top: 0;
}
.div3 {
  margin-bottom: 50px;
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




