<template>
  <div>
    <div v-for="(information, index) in informations" :key="index">
      <NuxtLink :to="'/informations/' + information.id" class="article1">
        <img class="im" :src="information.img" alt="img article" />
        <!-- <div class="im"></div> -->
        <div class="text">
          <h3>{{ information.title }}</h3>
          <p>{{ information.description }}</p>
        </div>
      </NuxtLink>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      informations: [],
    };
  },
  mounted() {
    this.$axios.$get("http://localhost:3003/Informations").then((resp) => {
      console.log(resp);
      this.informations = resp;
    });
  },
};
</script>

<style scoped>
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


