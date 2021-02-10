<template>
  <div>
    <div class="container">
      <div class="row">
        <div class="col-sm-8">
          <div class="card">
            <div class="card-header bg-success"><h1>Bienvenid@</h1></div>
            <div class="card-body">
              <h3 class="card-title">Que bueno que regresaste, verifica tu inventario y tus ultimos movimientos, no pierdas de vista tu inventario</h3>
            </div>
          </div>
        </div>
        <div class="col-sm-4">
          <div class="card">
            <div class="card-header bg-success"><h1>Recordatorio</h1></div>
            <div class="card-body">
              <h3 class="card-title">Plataforma</h3>
             <h4>   Desde este panel, puedes controlar todas tus categorias,
                articulos, productos y usuarios, puedes gestionar Roles,
                habilitar y desabilitar categorias y productos!</h4>
              
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import axios from "axios";
export default {
  name: "HelloWorld",
};
</script>
<style scoped>
</style>
