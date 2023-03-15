<template>
  <div class="text-start wrapper">
    <header>
      <div class="cus-container px-0 py-5">
        <div class="row">
          <h1 class="heading mb-4">Primary</h1>
          <div class="flex align-items-center justify-items-center">
            <a href="#kg" class="btn me-3 rounded-pill">
              kg
            </a>
            <a href="#year1" class="btn me-3 rounded-pill">
              year 1
            </a>
            <a href="#year2" class="btn me-3 rounded-pill">
              year 2
            </a>
            <a href="#year3" class="btn me-3 rounded-pill">
              year 3
            </a>
            <a href="#year4" class="btn me-3 rounded-pill">
              year 4
            </a>
            <a href="#year5" class="btn me-3 rounded-pill">
              year 5
            </a>
            <a href="#year6" class="btn me-3 rounded-pill">
              year 6
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
          id: 'kg',
          title: 'KG',
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
                'Phonics'
              ]
            },
            {
              title: 'Myanmar National Curriculum',
              lists: [
                'KG Level Subjects',
              ]
            },
            {
              title: 'Digital Learning for Skill Enhancement',
              lists: [
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
                'Yoga',
                'STEAM (Science, Technology, Engineering, Art & Maths)'
              ]
            },
          ]
        },
        {
          id: 'year1',
          title: 'YEAR 1',
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
                'PRIMARY Level Subjects',
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
                'Yoga',
                'STEAM (Science, Technology, Engineering, Art & Maths)'
              ]
            },
            {
              title: 'Foreign Language( Choose One )',
              lists: [
                'Chinese',
                'Japanese'
              ]
            },
          ]
        },
        {
          id: 'year2',
          title: 'YEAR 2',
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
                'PRIMARY Level Subjects',
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
                'Yoga',
                'STEAM (Science, Technology, Engineering, Art & Maths)'
              ]
            },
            {
              title: 'Foreign Language( Choose One )',
              lists: [
                'Chinese',
                'Japanese'
              ]
            },
          ]
        },
        {
          id: 'year3',
          title: 'YEAR 3',
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
                'PRIMARY Level Subjects',
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
                'Yoga',
                'STEAM (Science, Technology, Engineering, Art & Maths)'
              ]
            },
            {
              title: 'Foreign Language( Choose One )',
              lists: [
                'Chinese',
                'Japanese'
              ]
            },
          ]
        },
        {
          id: 'year4',
          title: 'YEAR 4',
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
                'PRIMARY Level Subjects',
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
                'Yoga',
                'STEAM (Science, Technology, Engineering, Art & Maths)'
              ]
            },
            {
              title: 'Foreign Language( Choose One )',
              lists: [
                'Chinese',
                'Japanese'
              ]
            },
          ]
        },
        {
          id: 'year5',
          title: 'YEAR 5',
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
                'PRIMARY Level Subjects',
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
                'Yoga',
                'Mindfulness',
                'STEAM (Science, Technology, Engineering, Art & Maths)'
              ]
            },
            {
              title: 'Foreign Language( Choose One )',
              lists: [
                'Chinese',
                'Japanese'
              ]
            },
          ]
        },
        {
          id: 'year6',
          title: 'YEAR 6',
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
                'PRIMARY Level Subjects',
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
                'Yoga',
                'Mindfulness',
                'STEAM (Science, Technology, Engineering, Art & Maths)'
              ]
            },
            {
              title: 'Foreign Language( Choose One )',
              lists: [
                'Chinese',
                'Japanese'
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