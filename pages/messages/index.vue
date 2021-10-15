<template>
  <section>
    <nav-component></nav-component>
    <div class="container">
      <div class="edit">
        <h3>Modifier</h3>
        <img src="../../assets/img/Composant 3 – 1.png" alt="img edit" class="imgEdit">
      </div>
      <h2>Messages</h2>
      <div class="search">
        <input type="text" placeholder="Rechercher">
      </div>
      <div class="message">
        <container-message :messages="messages"/>
      </div>
    </div>
  </section>
</template>

<script>
  export default {
    data(){
      return {
        messages: []
      }
    },
    mounted(){
      this.$axios.$get('http://localhost:3003/Messages')
      .then(resp => {
        console.log(resp)
        this.messages = resp
      })
    }
  }
</script>

<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Roboto&display=swap');
  *{
    font-family: Roboto;
  }
  .edit {
    display: flex;
    justify-content: space-between;
    align-items: center;
  }

  h3 {
    color: #505DFF;
    font-size: 20px;
  }

  h2 {
    font-size: 34px;
    font-weight: 700;
  }

  input {
    margin: 10px auto;
    width: 100%;
    background-color: #EEEEEE;
    border-radius: 10px;
    border: none;
    padding: 10px 15px;
  }

  .container {
    width: 95%;
    margin: 0 auto;
  }

  .imgEdit {
    width: 19px;
    height: 19px;
  }

</style>
