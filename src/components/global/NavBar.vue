<template>
  <div class="navbar">
    <figure class="logo">
      <img src="../../assets/images/drachma.svg" alt="">
    </figure>
    <div class="name">
      <p>
        Drachma
      </p>
    </div>
  </div>
</template>

<script>
export default {

}
</script>

<style scoped>
.navbar {
  box-sizing: border-box;
  background-color: #403B4F;
  height: 40px;
  width: 100%;
  padding-left: 10%;
  padding-right: 10%;
  font-family: Helvetica, sans-serif;
  color: #959595;
  display: flex;
  justify-content: flex-start;
}

.logo{
  margin: 0 40px 0 0;
  width: 40px;
  height: 40px;
}

.logo img{
  height: 100%;
  width: 100%;
}

.name{
  display: flex;
}

.name p{
  margin: auto;
  font-size: 20px;
}
</style>
