<template>
  <div>
    <footer>
      <div class="row bg-dark">
        <div class="col-sm-6">
          <div class="card ">
            <div class="card-body border border-success bg-dark text-center" >
              <img src="@/assets/icono/conection.png" alt="">
              <h5 class="card-title" style="color: white">
                Mas informacion de la compañia Team 170
              </h5>
              <p class="card-text" style="color: white">
                Lorem ipsum dolor sit amet, consectetur adipisicing elit.
                Accusantium dicta aperiam assumenda cupiditate blanditiis
                laudantium deleniti architecto. Voluptatibus hic molestias
                possimus, unde ad, minima, velit provident mollitia earum quos
                quis. Lorem ipsum dolor sit amet, consectetur adipisicing elit.
                
              </p>
              <a href="#" class="btn btn-outline-success btn-block">Nosotros</a>
            </div>
          </div>
        </div>
        <div class="col-sm-6">
          <div class="card">
            <div class="card-body border border-success bg-dark">
              <h5 class="card-title" style="color: white">
                Siguenos nuestro proyecto en GitHub
              </h5>
              <div class="list-group ">
                <a
                  href="https://github.com/JohanMolina-dev"
                  class="list-group-item list-group-item-action active"
                >
                  <div class="d-flex w-100 justify-content-between">
                    <h5 class="mb-1">Johan Sebastian Molina</h5>
                    <small>1 days ago</small>
                  </div>

                  <small>GitHub</small>
                </a>
                <h3 style="color: white">Contactanos</h3>
                <a
                  href="https://github.com/JohanMolina-dev"
                  class="list-group-item list-group-item-action "
                >
                  <div class="d-flex w-100 justify-content-between">
                    <h5 class="mb-1">Email:</h5>
                    <h6>este_emailesfalso@gmail.com</h6>
                    <small>1 days ago</small>
                  </div>

                  
                </a>
                <a
                  href="https://github.com/JohanMolina-dev"
                  class="list-group-item list-group-item-action "
                >
                  <div class="d-flex w-100 justify-content-between">
                    <h5 class="mb-1">Direccion</h5>
                    <h6>Avenida Pepito Juarez # 23 - 20</h6>
                    <small>1 days ago</small>
                  </div>

                  <small>Edificio Tech</small>
                </a>
                
              </div>
            </div>
          </div>
        </div>
      </div>
      <div class="container-footer">
        <div class="footer">
          <div class="copyright">
            © 2020 Todos los Derechos Reservados | <a href="">Team170</a>
          </div>

          <div class="information">
            <a href="">Informacion Compañia</a> |
            <a href="">Privacion y Politica</a> |
            <a href="">Terminos y Condiciones</a>
          </div>
        </div>
      </div>
    </footer>
  </div>
</template>

<script>
export default {
  name: "FooterBar",
};
</script>

<style scoped>
.container-footer-all {
  width: 100%;
  max-width: 1200px;
  margin: auto;
  padding: 40px;
  margin-top: 100px;
}
.footer {
  max-width: 1200px;
  margin: auto;
  display: flex;
  justify-content: space-between;
  padding: 20px;
}
.copyright {
  color: #c7c7c7;
}

.copyright a {
  text-decoration: none;
  color: white;
  font-weight: bold;
}

.information a {
  text-decoration: none;
  color: #c7c7c7;
}
.container-footer {
  width: 100%;
  background: #101010;
}
</style>