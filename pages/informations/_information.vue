<template>
  <div v-if="loading">
    <div class="div1">
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

    <p class="title">{{ information[0].title }}</p>
    <h1>{{ information[0].description }}</h1>
    <p class="author">Par {{ information[0].author }}</p>
    <p class="date">Publié le {{ information[0].date }}</p>

    <img class="foot" :src="information[0].img" alt="" />

    <p class="content">{{ information[0].content }}</p>

    <p class="content">{{ information[0].content1 }}</p>

    <p class="content">{{ information[0].content2 }}</p>

    <p class="content">{{ information[0].content3 }}</p>

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
  padding: 10px 10px;
  color: white;
  border-style: none;
  /* width: 100px;
  height: 30px; */
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
  margin-bottom: 60px;
}

.author {
  padding-left: 2%;
  padding-top: 5%;
  color: grey;
}
.date {
  padding-left: 2%;
  color: grey;
}
.title {
  padding-left: 2%;
  color: black;
}
.content {
  text-align: justify;
  margin-left: 5%;
  margin-right: 8%;
  color: black;
}
</style>
