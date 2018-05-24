<template>
  <div class="newsletter">
    <div class="form">
      <div class="text">
        <input type="email" class="input" placeholder="email@domain.com"><br>
        <button class="button">SUBSCRIBE</button>
      </div>
    </div>
  </div>
</template>

<script>
export default {

}
</script>

<style scoped>
.newsletter {
  position: relative;
  width: 100%;
  height: 300px;
  margin: 0;
  padding: 0;
  display: flex;
  align-content: center;
  align-items: center;
  background-image: url("../assets/images/servers.jpeg");
  background-attachment: fixed;
  background-repeat: no-repeat;
  background-size: cover;
  box-shadow: 0 10px 10px grey;
}

.form {
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
.form:before {
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
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  text-align: center;
  display: flex;
  justify-content: center;
  align-content: center;
  flex-wrap: wrap;
}

.input{
  width: 80%;
  height: 50px;
  text-align: center;
  margin: 5px;
  border-radius: 5%;
}

.button{
  width: 50%;
  border-radius: 5%;
  height: 50px;
  background-color: #88FCFC;
}
</style>
