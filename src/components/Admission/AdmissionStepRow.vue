<template>
  <div>
    <h6 class="sub-title text-uppercase mb-3">{{ row.title }}</h6>
    <div class="row">
      <div v-for="step in row.stepCards" :key="step.id" class="col">
        <div class="step">
          <div class="step-image" :class="step.img"></div>
          <p class="step-description text-capitalize" v-html="step.description"></p>
        </div>
      </div>
    </div>
  </div>
</template>

<script>

export default {
  props: {
    row: {
      type: Object
    }
  }
}
</script>

<style lang="scss" scoped>
.sub-title {
  font-size: var(--cus-fs-x-large);
  font-weight: var(--cus-fw-semibold);
  color: var(--cus-primary);
}

.step-description {
  font-weight: var(--cus-fw-semibold);
}

.step-image {
  background-size: contain;
  background-repeat: no-repeat;
  height: 140px;
}

// images
// bleow are jsut a bunch of images that point to src
// if you can change this into dynamic image bind with src, u should change.
.image-11 {
  background-image: url('@/assets/img/school/pre-school/1.png');
}
.image-12 {
  background-image: url('@/assets/img/school/pre-school/2.png');
}
.image-13 {
  background-image: url('@/assets/img/school/pre-school/3.png');
}
.image-14 {
  background-image: url('@/assets/img/school/pre-school/4.png');
}
.image-15 {
  background-image: url('@/assets/img/school/pre-school/5.png');
}
.image-16 {
  background-image: url('@/assets/img/school/pre-school/6.png');
}

.image-21 {
  background-image: url('@/assets/img/school/primary-secondary/1.png');
}
.image-22 {
  background-image: url('@/assets/img/school/primary-secondary/2.png');
}
.image-23 {
  background-image: url('@/assets/img/school/primary-secondary/3.png');
}
.image-23 {
  background-image: url('@/assets/img/school/primary-secondary/3.png');
}
.image-24 {
  background-image: url('@/assets/img/school/primary-secondary/4.png');
}
.image-25 {
  background-image: url('@/assets/img/school/primary-secondary/5.png');
}
.image-26 {
  background-image: url('@/assets/img/school/primary-secondary/6.png');
}

.image-27 {
  background-image: url('@/assets/img/school/primary-secondary/7.png');
}


.image-31 {
  background-image: url('@/assets/img/school/weekend-class/1.png');
}
.image-32 {
  background-image: url('@/assets/img/school/weekend-class/2.png');
}
.image-33 {
  background-image: url('@/assets/img/school/weekend-class/3.png');
}
.image-34 {
  background-image: url('@/assets/img/school/weekend-class/4.png');
}
.image-35 {
  background-image: url('@/assets/img/school/weekend-class/5.png');
}
.image-36 {
  background-image: url('@/assets/img/school/weekend-class/6.png');
}

.image-41 {
  background-image: url('@/assets/img/school/summer-class/1.png');
}
.image-42 {
  background-image: url('@/assets/img/school/summer-class/2.png');
}
.image-43 {
  background-image: url('@/assets/img/school/summer-class/3.png');
}
.image-44 {
  background-image: url('@/assets/img/school/summer-class/4.png');
}
.image-45 {
  background-image: url('@/assets/img/school/summer-class/5.png');
}
.image-46 {
  background-image: url('@/assets/img/school/summer-class/6.png');
}
</style>