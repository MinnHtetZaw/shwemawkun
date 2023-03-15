<template>
  <div class="text-start wrapper">
    <header>
      <div class="cus-container px-0 py-5">
        <div class="row">
          <h1 class="heading mb-4">International Primary</h1>
          <div class="flex align-items-center justify-items-center">
            <a href="#foundation" class="btn me-3 rounded-pill">
              foundation
            </a>
            <a href="#level1" class="btn me-3 rounded-pill">
              level-1
            </a>
            <a href="#level2" class="btn me-3 rounded-pill">
              level-2
            </a>
            <a href="#level3" class="btn me-3 rounded-pill">
              level-3
            </a>
            <a href="#level4" class="btn me-3 rounded-pill">
              level-4
            </a>
            <a href="#level5" class="btn me-3 rounded-pill">
              level-5
            </a>
            <a href="#level6" class="btn me-3 rounded-pill">
              level-6
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
          id: 'foundation',
          title: 'FOUNDATION/KG',
          subtitle: '<span class="text-cus-secondary">INTAKE</span> - <span class="text-cus-primary">JUNE & APRIL</span>',
          items: [
            {
              lists: [
                'English',
                'Mathematics',
                'Science',
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
                'Coding',
              ]
            },
          ]
        },
        {
          id: 'level1',
          title: 'pre starters',
          titleDetail: '(level-1)',
          subtitle: '<span class="text-cus-secondary">INTAKE</span> - <span class="text-cus-primary">JUNE & APRIL</span>',
          items: [
            {
              lists: [
                'English',
                'Mathematics',
                'Science',
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
                'Coding',
              ]
            },
          ]
        },
        {
          id: 'level2',
          title: 'starters',
          titleDetail: '(level-2)',
          subtitle: '<span class="text-cus-secondary">INTAKE</span> - <span class="text-cus-primary">JUNE & APRIL</span>',
          items: [
            {
              lists: [
                'English',
                'Mathematics',
                'Science',
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
                'Coding',
              ]
            },
          ]
        },
        {
          id: 'level3',
          title: 'movers',
          titleDetail: '(level-3)',
          subtitle: '<span class="text-cus-secondary">INTAKE</span> - <span class="text-cus-primary">JUNE & APRIL</span>',
          items: [
            {
              lists: [
                'English',
                'Mathematics',
                'Science',
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
                'Coding',
              ]
            },
          ]
        },
        {
          id: 'level4',
          title: 'pre flyers',
          titleDetail: '(level-4)',
          subtitle: '<span class="text-cus-secondary">INTAKE</span> - <span class="text-cus-primary">JUNE & APRIL</span>',
          items: [
            {
              lists: [
                'English',
                'Mathematics',
                'Science',
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
                'Coding',
              ]
            },
          ]
        },
        {
          id: 'level5',
          title: 'a2 keys',
          titleDetail: '(ket foundation, level-5)',
          subtitle: '<span class="text-cus-secondary">INTAKE</span> - <span class="text-cus-primary">JUNE & APRIL</span>',
          items: [
            {
              lists: [
                'English',
                'Mathematics',
                'Science',
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
                'Coding',
              ]
            },
          ]
        },
        {
          id: 'level6',
          title: 'a2 keys',
          titleDetail: '(ket, level-6)',
          subtitle: '<span class="text-cus-secondary">INTAKE</span> - <span class="text-cus-primary">JUNE & APRIL</span>',
          items: [
            {
              lists: [
                'English',
                'Mathematics',
                'Science',
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
                'Coding',
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