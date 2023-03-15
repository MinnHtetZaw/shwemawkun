<template>
  <div class="text-start wrapper">
    <header>
      <div class="cus-container px-0 py-5">
        <div class="row">
          <h1 class="heading mb-4">Secondary</h1>
          <div class="flex align-items-center justify-items-center">
            <a href="#year7" class="btn me-3 rounded-pill">
              year 7
            </a>
            <a href="#year8" class="btn me-3 rounded-pill">
              year 8
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
          id: 'year7',
          title: 'YEAR 7',
          subtitle: '<span class="text-cus-secondary">INTAKE</span> - <span class="text-cus-primary">JUNE</span>',
          items: [
            {
              title: 'International Curriculum',
              lists: [
                'English',
                'Myanmar',
                'Science',
                'Computing',
                'Global Citizenship',
              ]
            },
            {
              title: 'Myanmar National Curriculum',
              lists: [
                'Middle Level Subjects',
              ]
            },
            {
              title: 'Digital Learning for Skill Enhancement',
              lists: [
                'English',
                'Maths',
                'Science',
                'Coding',
              ]
            },
            {
              title: 'Co-Curicular Activities',
              lists: [
                'Arts',
                'Physical Education',
                'Music',
                'Mindfulness',
                'Myanmar Dance',
                'STEAM (Science, Technology, Engineering, Art & Maths)'
              ]
            },
          ]
        },
        {
          id: 'year8',
          title: 'YEAR 8',
          subtitle: '<span class="text-cus-secondary">INTAKE</span> - <span class="text-cus-primary">JUNE</span>',
          items: [
            {
              title: 'International Curriculum',
              lists: [
                'English',
                'Myanmar',
                'Science',
                'Computing',
                'Global Citizenship',
              ]
            },
            {
              title: 'Myanmar National Curriculum',
              lists: [
                'Middle Level Subjects',
              ]
            },
            {
              title: 'Digital Learning for Skill Enhancement',
              lists: [
                'English',
                'Maths',
                'Science',
                'Coding',
              ]
            },
            {
              title: 'Co-Curicular Activities',
              lists: [
                'Arts',
                'Physical Education',
                'Music',
                'Mindfulness',
                'Myanmar Dance',
                'STEAM (Science, Technology, Engineering, Art & Maths)'
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