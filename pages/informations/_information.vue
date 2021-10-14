<template>
  <div v-if="loading">
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

    <p>{{ information[0].title }}</p>
    <h1>{{ information[0].description }}</h1>
    <p>Par {{ information[0].author }}</p>
    <p>Publié le {{ information[0].date }}</p>

    <img class="foot" :src="information[0].img" alt="" />

    <p>{{ information[0].content }}</p>

    <p>{{ information[0].content1 }}</p>

    <p>{{ information[0].content2 }}</p>

    <p>{{ information[0].content3 }}</p>

    <footer>
      <img class="foot" src="../../assets/img/Footer.png" alt="" />
    </footer>
  </div>
</template>

<script>
export default {
  data() {
    return {
      information: [],
      loading: false,
    };
  },
  async mounted() {
    var id = this.$route.params.information;
    console.log(id);
    var informationGet = await this.$axios.$get(
      "http://localhost:3003/Informations?id=" + id
    );
    this.information = informationGet;
    this.loading = true;
    console.log(this.information);
  },
};
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

.foot {
  width: 100%;
  height: auto;
  margin-bottom: 6©©0px;
}
</style>
