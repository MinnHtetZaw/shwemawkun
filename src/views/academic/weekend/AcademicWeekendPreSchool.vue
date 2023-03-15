<template>
  <div class="text-start wrapper">
    <header>
      <div class="cus-container px-0 py-5">
        <div class="row">
          <h1 class="heading mb-4">PRE-SCHOOL/EARLY YEAR</h1>
          <div class="flex align-items-center justify-items-center">
            <a href="#Nusery" class="btn me-3 rounded-pill">
              nusery
            </a><a href="#prekg" class="btn me-3 rounded-pill">
              PRE-KG
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
          id: 'Nusery',
          title: 'NUSERY',
          subtitle: '<span class="text-cus-secondary">INTAKE</span> - <span class="text-cus-primary">JUNE & APRIL</span>',
          items: [
            {
              lists: ['1) Communication and Language (English)']
            },
            {
              lists: ['2) Literacy(English)'],
            },
            {
              lists: ['3) Personal, Social, Health and Emotional Development Life Skills Personal Hygiene'],
            },
            {
              lists: ['4) Physical Development Fine & Gross Motor Skills'],
            }, 
            {
              lists: ['5) Numeracy / Mathematics'],
            },
            {
              lists: ['Digital Learning for Skill Enhancement'],
            },
            {
              lists: [
                'Mathematics',
                'English',
                'Phonics',
              ],
            },
          ]
        },
        {
          id: 'prekg',
          title: 'PRE-KG ',
          subtitle: '<span class="text-cus-secondary">INTAKE</span> - <span class="text-cus-primary">JUNE & APRIL</span>',
          items: [
            {
              lists: ['1) Communication and Language (English)']
            },
            {
              lists: ['2) Literacy(English)'],
            },
            {
              lists: ['3) Personal, Social, Health and Emotional Development Life Skills Personal Hygiene'],
            },
            {
              lists: ['4) Physical Development Fine & Gross Motor Skills'],
            },
            {
              lists: ['5) Numeracy / Mathematics'],
            },
            {
              lists: ['Digital Learning for Skill Enhancement'],
            },
            {
              lists: [
                'Mathematics',
                'English',
                'Phonics',
              ],
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