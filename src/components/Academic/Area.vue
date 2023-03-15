<template>
  <div class="row bg-white border-bottom course-row">
    <div class="col-6">
      <div class="d-flex flex-column justify-content-center h-100 area-title-wrapper">
        <div>
          <h1 class="title">{{ area.title }}</h1>
          <h3 v-if="area.titleDetail" class="title-detail">{{ area.titleDetail }}</h3>
          <h2 class="subtitle" v-html="area.subtitle"></h2>
        </div>
      </div>
    </div>
    <div class="col-6">
      <div :id="area.id" class="course d-flex flex-column justify-content-center h-100">
        <AreaItem
          v-for="(item, index) in area.items"
          :data="item"
          :index="index"
          :key="index"
        ></AreaItem>
      </div>
    </div>
  </div>
</template>

<script>
import AreaItem from "@/components/Academic/AreaItem.vue";
export default {
  components: {
    AreaItem,
  },
  props: {
    area: Object,
  },
};
</script>

<style lang="scss" scoped>
.area-title-wrapper {
  margin-left: 15%;
}

.title {
  display: inline-block;
  text-transform: uppercase;
  font-weight: var(--cus-fw-semibold);
  color: var(--cus-primary);
  font-size: var(--cus-fs-xxxx-large);
  margin-right: 5px;
}

.title-detail {
  text-transform: uppercase;
  display: inline-block;
  font-weight: var(--cus-fw-semibold);
  color: var(--cus-primary);
  font-size: var(--cus-fs-xx-large);
}

.subtitle {
  text-transform: uppercase;
  font-weight: var(--cus-fw-semibold);
  color: var(--cus-primary);
  font-size: var(--cus-fs-x-large);
}

.course {
  padding: 20px 0;
}

.course-row {
  min-height: 200px;
}
</style>
