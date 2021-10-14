<template>
  <div class="content">
    <img src="#" alt="img profil message">
    <div>
      <hr>
      <div class="align-flex">
      <h2>Prune</h2>
      <h3>14:54 ></h3>
      </div>
      <p>Il y a eu un accident sur l'autoroute...</p>
      <hr>
    </div>
  </div>
</template>

<style scoped>
  img {
    width: 60px;
    height: 60px;
    border-radius: 60px;
  }
  h2{
    font-size: 18px;
    color: black;
    font-weight: 700;
  }
  p{
    font-size: 16px;
    color: #7C7C7C;
    font-weight: 400;
  }
  h3{
    font-size: 16px;
    color: #7C7C7C;
    font-weight: 400;
  }
  .align-flex{
    display: flex;
    justify-content: space-between;
    align-items: center;
  }
  .content{
    display: flex;
    justify-content: space-between;
    padding: 20px;
    align-items: center;
  }
</style>
