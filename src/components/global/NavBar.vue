<template>
  <div class="navbar">
    <figure class="logo">
      <img src="../../assets/images/drachma.svg" alt="" @click="$router.push('/')">
    </figure>
    <div class="name">
      <p @click="$router.push('/')">
        Drachma
      </p>
    </div>
    <div class="name">
      <p @click="$router.push('/graph')">
        Precio
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
  cursor: pointer;
}

.logo img{
  height: 100%;
  width: 100%;
  cursor: pointer;
}

.name{
  display: flex;
  margin: 0 40px 0 0;
  cursor: pointer;
}

.name p{
  margin: auto;
  font-size: 20px;
  cursor: pointer;
}
</style>
