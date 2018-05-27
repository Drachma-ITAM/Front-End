<template>
  <div class="info w3-grey">
    <div class="label">
      <div class="text">
        <p>Helping you being up to date</p>
        <p>with every cryptocurrency</p>
        <p>out there!</p>
      </div>
    </div>
    <div class="label">
      <div class="text">
        <p>Don´t forget to subscribe to our</p>
        <p>newsletter and get every update</p>
        <p>you might need to</p>
        <p>boost your cryptocurrency</p>
        <p>curiosity!</p>
      </div>
    </div>
  </div>
</template>

<script>
export default {

}
</script>

<style scoped>
.info{
  height: 300px;
  width: 100%;
  display: flex;
  justify-content: space-evenly;
  align-items: center;
  background-color: lightgrey;
  flex-wrap: wrap;
  box-shadow: inset 0 0 0 200px rgba(10, 0, 0, 0.08);
}

.label{
  box-sizing: border-box;
  background-color: white;
  padding: 15px;
  border-radius: 30%;
  height: 220px;
  display: flex;
  justify-content: center;
  align-content: center;
}

.text{
  margin: auto;
}

@media only screen  and (max-width: 519px){
  .info{
    height: 550px;
  }
}
</style>
