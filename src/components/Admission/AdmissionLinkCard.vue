<template>
  <div>
    <div class="card cus_card">
      <div class="image_holder" :class="card.class">
          <router-link :to="{name: card.url}" class="image_title text-uppercase">{{ card.title }}</router-link>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    card: {
      type: Object,
    }
  }
}
</script>

<style lang="scss" scoped>
.image_title {
  position: absolute;
  bottom: 0;
  width: 100%;
  font-weight: var(--cus-fw-semibold);
  padding: 12px 0;
  color: var(--cus-primary);
  background-color: var(--cus-secondary);
  text-decoration: none;
  display: block;
}

.image_holder {
  background-position: 70% center;
  background-size: cover;
  background-repeat: no-repeat;
  position: relative;
  width: auto;
  height: 250px;
}

.cus_card {
  border-radius: 0;
  height: 250px;
}

// images
.image-1 {
  background-image: url('@/assets/img/photo/01.png');
}

.image-2 {
  background-image: url('@/assets/img/photo/02.png');
}

.image-3 {
  background-image: url('@/assets/img/photo/04.png');
}

.image-4 {
  background-image: url('@/assets/img/photo/05.png');
}
</style>