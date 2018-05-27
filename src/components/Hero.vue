<template>
  <div class="hero">
    <div class="slogan">
      <p class="text">Never miss a price.</p>
    </div>
  </div>
</template>

<script>
export default {

}
</script>

<style scoped>
.hero {
  position: relative;
  width: 100%;
  height: 400px;
  margin: 0;
  padding: 0;
  display: flex;
  align-content: center;
  align-items: center;
  background-image: url("../assets/images/bg.jpeg");
  background-attachment: fixed;
  background-repeat: no-repeat;
  background-size: cover;
  box-shadow: 0 10px 10px grey;
}

.slogan {
  position: absolute;
  width: 45%;
  height: 150px;
  top: 100px;
  left: 25%;
  margin: 0;
  padding: 0;
  background: inherit;
  overflow: hidden;
  border-radius: 15%;
  display: flex;
  align-content: center;
  align-items: center;
}
.slogan:before {
  position: absolute;
  height: 150px;
  content: "";
  background: inherit; 
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  box-shadow: inset 0 0 0 200px rgba(10, 0, 0, 0.08);
  filter: blur(10px);
  border-radius: 15%;
}

.text {
  position: absolute;
  width: 100%;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  text-align: center;
  font-size: 50px;
  margin: 45px 0;
  color: #88FCFC;
}

@media only screen  and (max-width: 1010px){
  .text {
    font-size: 35px;
  }
}

@media only screen  and (max-width: 670px){
  .text {
    font-size: 25px;
  }
}
</style>
