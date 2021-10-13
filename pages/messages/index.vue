<template>
  <section>
    <div class="edit">
      <h3>Modifier</h3>
      <h3>Edit</h3>
    </div>
    <h2>Messages</h2>
    <div class="search">
      <input type="text" placeholder="Rechercher">
    </div>
    <div class="message">
      <container-message></container-message>
    </div>
  </section>
</template>

<script>

</script>

<style scoped>
.edit{
  display: flex;
  justify-content: space-between;
}
h3{
  color: #505DFF;
  font-size: 20px;
}
h2{
  font-size: 34px;
  font-weight: 700;
}
input{
  width: 100%;
  background-color: #EEEEEE;
  border-radius: 10px;
  border: none;
  padding: 10px 15px;
}
section {
  width: 90%;
  margin: 0 auto;
}
</style>

