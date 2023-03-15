<template>
  <div class="text-start wrapper">
    <header>
      <div class="cus-container px-0 py-5">
        <div class="row">
          <h1 class="heading mb-4">International Secondary</h1>
          <div class="flex align-items-center justify-items-center">
            <a href="#level7" class="btn me-3 rounded-pill">
              level-7
            </a>
            <a href="#level8" class="btn me-3 rounded-pill">
              level-8
            </a>
            <a href="#level9" class="btn me-3 rounded-pill">
              level-9
            </a>
            <a href="#cae" class="btn me-3 rounded-pill">
              cae
            </a>
          </div>
        </div>
      </div>
    </header>

    <div class="cus-container px-3 pb-5">
      <div class="course-list">
        <div class="row label-bar">
          <div class="col-6">
            <div class="label py-3 text-uppercase text-center">
              intake
            </div>
          </div>
          <div class="col-6">
            <div class="label py-3 text-uppercase">area of learning</div>
          </div>
        </div>
        <Area v-for="area in payload" :area="area"></Area>
      </div>
    </div>

    <div class="container-fluid videos-wrapper p-3">
      <div class="row">
        <div class="col-4">
          <div class="video">
          </div>
        </div>
        <div class="col-4">
          <div class="video">
          </div>
        </div>
        <div class="col-4">
          <div class="video">
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import Area from '@/components/Academic/Area.vue'
export default {
  components: {
    Area
  },
  data() {
    return {
      payload: [
        {
          id: 'level7',
          title: 'B1 PRELIMINARY',
          titleDetail: '(PET FOUNDATION, LEVEL-7)',
          subtitle: '<span class="text-cus-secondary">INTAKE</span> - <span class="text-cus-primary">JUNE & APRIL</span>',
          items: [
            {
              lists: [
                'English',
                'Mathematics',
                'Computing',
                'Global Citizenship',
              ]
            },
            {
              lists: [
                'Digital Learning for Skill Enhancement',
              ]
            },
            {
              lists: [
                'Mathematics',
                'English',
                'Science',
                'Coding',
              ]
            },
          ]
        },
        {
          id: 'level8',
          title: 'B1 PRELIMINARY',
          titleDetail: '(PET, LEVEL-8)',
          subtitle: '<span class="text-cus-secondary">INTAKE</span> - <span class="text-cus-primary">JUNE & APRIL</span>',
          items: [
            {
              lists: [
                'English',
                'Mathematics',
                'Computing',
                'Global Citizenship',
              ]
            },
            {
              lists: [
                'Digital Learning for Skill Enhancement',
              ]
            },
            {
              lists: [
                'Mathematics',
                'English',
                'Science',
                'Coding',
              ]
            },
          ]
        },
        {
          id: 'level9',
          title: 'B1 FIRST',
          titleDetail: '(FEC FOUNDATION, LEVEL-9)',
          subtitle: '<span class="text-cus-secondary">INTAKE</span> - <span class="text-cus-primary">JUNE & APRIL</span>',
          items: [
            {
              lists: [
                'English',
              ]
            },
          ]
        },
        {
          id: 'cae',
          title: 'C1 ADVANCED',
          titleDetail: '(CAE)',
          subtitle: '<span class="text-cus-secondary">INTAKE</span> - <span class="text-cus-primary">JUNE & APRIL</span>',
          items: [
            {
              lists: [
                'English',
              ]
            },
          ]
        },
      ]
    }
  }
}
</script>

<style lang="scss" scoped>
.wrapper {
  background-color: var(--cus-primary);
}

.heading {
  text-transform: uppercase;
  color: var(--cus-secondary);
  font-weight: var(--cus-fw-semibold);
}

.btn {
  background-color: var(--cus-white);
  min-width: 90px;
  text-transform: uppercase;
  color: var(--cus-primary)
}

.label-bar {
  background-color: var(--cus-grey);
  border-bottom: 1px solid #808080;

  .label {
    font-size: var(--cus-fs-large);
    color: var(--cus-secondary-bold);
    font-weight: var(--cus-fw-semibold);
  }
}

.course-list {
  background-color: var(--cus-white);
}

.video {
  background-color: white;
  width: 100%;
  height: 300px;
}

.videos-wrapper {
  background-color: var(--cus-grey);
}
</style>