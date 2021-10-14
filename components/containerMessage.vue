<template>
  <div>
    <div v-for="(message, index) in messages" :key="index">
    <NuxtLink :to="'/messages/'+message.id" class="content">
      <div class="circle"></div>
      <img :src="message.img" alt="img profil message">
      <div class="containerLeft">
        <hr>
        <div class="align-flex">
          <h2>{{message.nom}}</h2>
          <h3>{{message.heure}} ></h3>
        </div>
        <p>{{message.last}}</p>
      </div>
    </NuxtLink>
    </div>
  </div>
</template>

<script>
  export default {
    props: [
      'messages'
    ],
    data() {
      return {

      }
    },
    mounted() {

    }
  }

</script>


<style scoped>
  @import url('https://fonts.googleapis.com/css2?family=Roboto&display=swap');
  *{
    font-family: Roboto;
  }
  img {
    width: 60px;
    height: 60px;
    border-radius: 60px;
  }

  h2 {
    font-size: 18px;
    color: black;
    font-weight: 700;
  }

  p {
    font-size: 16px;
    color: #7C7C7C;
    font-weight: 400;
  }

  h3 {
    font-size: 16px;
    color: #7C7C7C;
    font-weight: 400;
  }

  .align-flex {
    display: flex;
    justify-content: space-between;
    align-items: center;
  }

  .content {
    display: flex;
    justify-content: space-between;
    align-items: center;
  }

  .circle {
    width: 15px;
    height: 15px;
    border-radius: 40px;
    background-color: #505DFF;
  }
  hr{
    margin-top: 0;
  }
  .containerLeft{
    width: 73%;
  }

</style>
