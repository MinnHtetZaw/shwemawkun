<template>
  <div class="course-item">
    <h5 v-if="data.title" class="title text-capitalize">{{ data.title }}</h5>
    <div v-if="data.lists">
      <div class="item" v-for="(list, index) in data.lists" :key="index">{{ list }}</div>
      <!-- <div>English</div>
      <div>Math</div>
      <div>Science</div>
      <div>Computing</div>
      <div>Global Citzenship</div>
      <div>Phonics</div> -->
    </div>
  </div>
</template>

<script>
export default {
  props: {
    data: Object,
    index: [String,Number],
  }
}
</script>

<style lang="scss" scoped>
.course-item {
  &:not(:last-child) {
    padding: 0 0 20px 0;
  }

  .title {
    color: var(--cus-primary);
    font-weight: var(--cus-fw-semibold);
  }

  .item {
    color: var(--cus-primary);
    font-size: var(--cus-fs-large);
  }
}
</style>