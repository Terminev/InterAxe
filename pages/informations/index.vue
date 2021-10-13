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

    <div class="div3">
      <img src="" alt="" />
      <div class="div3a">Le XV de France s'impose face aux Allblacks</div>
    </div>
    <br />
    <br />
    <div class="article">
      <div class="section 1">
        <div class="article1">
          <div class="im"></div>
          <div class="text">
            <h3>NUCLÉAIRE, HYDROGÈNE ET RENOUVELABLES :</h3>
            <p>LE PLAN DE MACRON POUR L'ÉNERGIE EN 2030</p>
          </div>
        </div>

        <div class="article1">
          <div class="im"></div>
          <div class="text">
            <h3>DISPARITIONS :</h3>
            <p>ACCIDENT MORTEL SUR L'AUTOROUTE A7</p>
          </div>
        </div>

        <div class="article1">
          <div class="im"></div>
          <div class="text">
            <h3>PARIS:</h3>
            <p>6000 ÉCOLIERS EN MOINS EN UN AN, UNE BAISSE INÉDITE</p>
          </div>
        </div>
      </div>

      <div class="section2">
        <div class="article1">
          <div class="im"></div>
          <div class="text">
            <h3>GRÈCE:</h3>
            <p>SÉISME DE 6,3 AU LARGE DE LA CRÈTE</p>
          </div>
        </div>

        <div class="article1">
          <div class="im"></div>
          <div class="text">
            <h3>MOUSTIQUES:</h3>
            <p>
              POURQUOI PROLIFÈRENT-ILS ENCORE MALGRÉ L'ARRIVÉE DE L'AUTOMNE?
            </p>
          </div>
        </div>

        <div class="article1">
          <div class="im"></div>
          <div class="text">
            <h3>PARIS:</h3>
            <p>6000 ÉCOLIERS EN MOINS EN UN AN, UNE BAISSE INÉDITE</p>
          </div>
        </div>
      </div>
    </div>
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
  /* border-radius: 10% 5; */
  height: 30px;
  width: 200px;
}
.menu ul {
  display: flex;
  justify-content: space-around;
  list-style-type: none;
}
h1 {
  padding-left: 2%;
  padding-top: 5%;
}
.div3 {
  background-color: #505dff;
  height: 100px;
}
.div3a {
  background-color: white;
  opacity: 0, 33;
  margin-top: 50px;
}
.article {
  display: flex;
  justify-content: space-between;
}
.article1 {
  display: flex;
  justify-content: start;
  margin-bottom: 20px;
}
.im {
  width: 100px;
  height: 100px;
  background-color: yellow;
  padding-top: 20px;
  border-radius: 20%;
  margin-left: 20px;
}
h3 {
  font-size: 20px;
}
.text {
  margin-left: 20px;
}
</style>




