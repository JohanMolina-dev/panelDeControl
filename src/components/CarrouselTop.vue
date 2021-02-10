<template>
  <div>
    
   <div id="carouselExampleFade" class="carousel slide carousel-fade" data-ride="carousel">
  <div class="carousel-inner">
    <div class="carousel-item active">
      <img src="@/assets/imagenes/herramientas.jpg" class="d-block w-100" alt="Una Imagen de prueba" style="width:650px;height:450px">
    </div>
    <div class="carousel-item">
      <img src="@/assets/imagenes/herramientas2.jpg" class="d-block w-100" alt="..." style="width:650px;height:450px">
    </div>
    <div class="carousel-item">
      <img src="@/assets/imagenes/herramientas3.jpg" class="d-block w-100" alt="..." style="width:650px;height:450px">
    </div>
  </div>
  <a class="carousel-control-prev" href="#carouselExampleFade" role="button" data-slide="prev">
    <span class="carousel-control-prev-icon" aria-hidden="true"></span>
    <span class="sr-only">Anterior</span>
  </a>
  <a class="carousel-control-next" href="#carouselExampleFade" role="button" data-slide="next">
    <span class="carousel-control-next-icon" aria-hidden="true"></span>
    <span class="sr-only">Siguiente</span>
  </a>
</div>
<hr>
  </div>
</template>

<script>
export default {
  name: "CarrouselTop",
};
</script>

<style scoped>
</style>
