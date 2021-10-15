<template>
  <div class="container" v-if="loading">
    <nav-component />
    <div class="header">
      <NuxtLink :to="'/messages'" class="infos">
        <h2>
          < </h2> <p>32</p>
      </NuxtLink>
      <div>
        <img :src="user[0].img" alt="img profil">
        <h3>{{user[0].nom}} ></h3>
      </div>
      <div class="spacer">

      </div>
    </div>
    <div class="messages">
      <div v-for="(message, index) in user[0].Message" :key="index">
        <div v-if="message.me == 1" class="me">
          <p>{{message.contenus}}</p>
        </div>

        <div v-if="message.me == 0" class="you">
          <p>{{message.contenus}}</p>
        </div>
      </div>

    </div>
    <div class="comment">
      <input type="text" placeholder="PulvMessage...">
      <img src="../../assets/img/Icon ionic-ios-arrow-dropup-circle.png" alt="img send" class="send">
    </div>
  </div>
</template>

<script>
  export default {
    data() {
      return {
        user: [],
        loading: false,
      }
    },
    async mounted() {
      var id = this.$route.params.message
      var userGet = await this.$axios.$get('http://localhost:3003/Messages?id=' + id)
      this.user = userGet
      this.loading = true
    },
  }

</script>

<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Roboto&display=swap');
  *{
    font-family: Roboto;
  }
  .infos {
    display: flex;
    align-items: center;
  }

  .infos p {
    color: white;
    font-size: 16px;
    background-color: #505DFF;
    padding: 5px 10px;
    border-radius: 40px;
    margin: auto 0;
  }

  h2 {
    font-size: 22px;
    margin-right: 5px;
    color: #7C7C7C;
  }

  .header {
    width: 90%;
    display: flex;
    justify-content: space-between;
    margin: 20px auto;
  }

  img {
    width: 60px;
    height: 60px;
  }

  h3 {
    color: #7C7C7C;
    font-size: 16px;
    text-align: center;
  }

  .spacer {
    width: 58px;
  }

  .messages {
    margin-top: 50px;
    height: 60vh;
    overflow-y: scroll;
  }

  .you {
    background-color: #EEEEEE;
    padding: 10px 15px;
    border-radius: 15px;
    font-size: 16px;
    margin-bottom: 15px;
    width: fit-content;
    max-width: 74%;
    clear: right;
  }

  .me {
    background-color: #505DFF;
    padding: 10px 15px;
    border-radius: 15px;
    color: white;
    font-size: 16px;
    margin-bottom: 15px;
    width: fit-content;
    max-width: 74%;
    float: right;
  }
  p {
    margin-bottom: 0;
  }
  .comment input{
    width: 100%;
    border-radius: 40px;
    padding: 10px 15px;
    border: solid 1px #7C7C7C;
  }
  .comment{
    position: relative;
  }
  .send{
    width: fit-content;
    position: absolute;
    width: 30px;
    height: 30px;
    right: 15px;
    top: 8px;
  }

</style>
