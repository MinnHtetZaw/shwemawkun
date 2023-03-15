<template>
  <div class="card_container">
    <div class="card cus_card">
      <div class="card-body p-5">
        <div class="content_container shadow">
          <h1 class="text-uppercase">Admission overview</h1>
          <p>
            Lorem ipsum dolor sit amet, consectetur adipisicing elit. Eius totam dolores maxime atque? Quia id harum,
            quod, omnis eum ullam maiores molestiae necessitatibus, vero soluta sequi molestias voluptatibus. Harum,
            quibusdam? Lorem ipsum dolor sit amet, consectetur adipisicing elit. Eius totam dolores maxime atque? Quia
            id harum, quod, omnis eum ullam maiores molestiae necessitatibus, vero soluta sequi molestias voluptatibus.
            Harum, quibusdam?Lorem ipsum dolor sit amet, consectetur adipisicing elit. Eius totam dolores maxime atque?
            Quia id harum, quod, omnis eum ullam maiores molestiae necessitatibus, vero soluta sequi molestias
            voluptatibus. Harum, quibusdam?Lorem ipsum dolor sit amet, consectetur adipisicing elit. Eius totam dolores
            maxime atque? Quia id harum, quod, omnis eum ullam maiores molestiae necessitatibus, vero soluta sequi
            molestias voluptatibus. Harum, quibusdam?Lorem ipsum dolor sit amet, consectetur adipisicing elit. Eius
            totam dolores maxime atque? Quia id harum, quod, omnis eum ullam maiores molestiae necessitatibus, vero
            soluta sequi molestias voluptatibus. Harum, quibusdam?
          </p>
        </div>
        <div class="image_contianer">
          <div class="image" alt=""></div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {

}
</script>

<style lang="scss" scoped>
.cus_card {
  width: 100%;
  background-color: var(--cus-primary);
  border-radius: 0 !important;
}

.content_container {
  position: relative;
  z-index: 20;
  padding: 30px 30px;
  width: 55%;
  height: 100%;
  background-color: var(--cus-secondary);

  h1 {
    font-weight: bolder;
    margin-bottom: 30px;
  }

  p {
    text-align: justify;
  }
}

.image {
  background-image: url('@/assets/img/photo/03.png');
  background-position: 70% center;
  background-size: cover;
  background-repeat: no-repeat;
  position: absolute;
  top: 50%;
  transform: translateY(-50%);
  right: 48px;
  width: 550px;
  height: 550px;
}

img {
  z-index: 5;
}
</style>