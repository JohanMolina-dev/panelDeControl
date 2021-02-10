<template>
  <div>
    <hr>
        <br> <br> <br>
        
    <div class="card border-success mb-3" style="max-width: 18rem" id="container1" >
      <div id="ex2">
      <img :src="member.image" class="card-img-top" alt="..." />
      </div>
      <div class="card-header bg-transparent border-success">Codigo: {{member.codigo}} </div>
      <div class="card-body text-success">
        <h5 class="card-title"> {{member.nombre}} </h5>
        <p class="card-text">
         {{member.descripcion}}
        </p>
      </div>
      <div class="card-footer bg-transparent border-success">Rol: {{member.rol}} </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "TeamCard",
  props: ["member"],
};
</script>

<style scoped>

#container1 {
width: 300px;
margin: 0 auto;
}
.ex2 img{
height: 100px;
width: 300px;
margin: 15px 0;
-webkit-transition: all 1s ease;
-moz-transition: all 1s ease;
-ms-transition: all 1s ease;
transition: all 1s ease;
}
.ex2 img:hover {
height: 133px;
width: 400px;
margin-left: -50px;
}
</style>
