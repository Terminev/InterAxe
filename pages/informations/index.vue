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
      <div class="article1">
        <img class="im" src="../../assets/img/EM.jpg" alt="" />
        <!-- <div class="im"></div> -->
        <div class="text">
          <h3>NUCLÉAIRE, HYDROGÈNE ET RENOUVELABLES :</h3>
          <p>LE PLAN DE MACRON POUR L'ÉNERGIE EN 2030</p>
        </div>
      </div>

      <div class="article1">
        <img src="" alt="" />
        <img class="im" src="../../assets/img/accident.jpg" alt="" />
        <div class="text">
          <h3>DISPARITIONS :</h3>
          <p>ACCIDENT MORTEL SUR L'AUTOROUTE A7</p>
        </div>
      </div>

      <div class="article1">
        <img class="im" src="../../assets/img/ecole.jpg" alt="" />
        <div class="text">
          <h3>PARIS:</h3>
          <p>6000 ÉCOLIERS EN MOINS EN UN AN, UNE BAISSE INÉDITE</p>
        </div>
      </div>

      <div class="article1">
        <img class="im" src="../../assets/img/grece.jpg" alt="" />
        <div class="text">
          <h3>GRÈCE:</h3>
          <p>SÉISME DE 6,3 AU LARGE DE LA CRÈTE</p>
        </div>
      </div>

      <div class="article1">
        <img class="im" src="../../assets/img/moustique.jpg" alt="" />
        <div class="text">
          <h3>MOUSTIQUES:</h3>
          <p>POURQUOI PROLIFÈRENT-ILS ENCORE MALGRÉ L'ARRIVÉE DE L'AUTOMNE?</p>
        </div>
      </div>

      <div class="article1">
        <img class="im" src="../../assets/img/naturalisation.jpg" alt="" />
        <div class="text">
          <h3>"IL A PLEINEMENT SA PLACE EN FRANCE":</h3>
          <p>L'APPEL D'UNE FEMME SAUVÉE PAR UN DEMANDEUR D'ASILE GUINÉEN</p>
        </div>
      </div>

      <div class="article1">
        <img class="im" src="../../assets/img/ME.jpg" alt="" />
        <div class="text">
          <h3>FRANCE 2030:</h3>
          <p>
            A QUOI SERVIRONT LES 30 MILLIARDS D'EUROS ANNONCÉS PAR EMMANUEL
            MACRON?
          </p>
        </div>
      </div>
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




