<template>
  <div class="text-start wrapper">
    <header>
      <div class="cus-container px-0 py-5">
        <div class="row">
          <h1 class="heading mb-4">Pre-school(Early years)</h1>
          <div class="flex align-items-center justify-items-center">
            <a href="#Nusery1" class="btn me-3 rounded-pill">
              nusery 1
            </a><a href="#Nusery2" class="btn me-3 rounded-pill">
              nusery 2
            </a>
            <a href="#prekg1" class="btn me-3 rounded-pill">
              pre-kg 1
            </a>
            <a href="#prekg2" class="btn me-3 rounded-pill">
              pre-kg 2
            </a>
            <a href="#prekg3" class="btn me-3 rounded-pill">
              pre-kg 3
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
          id: 'Nusery1',
          title: 'NUSERY 1',
          subtitle: '<span class="text-cus-secondary">INTAKE</span> - <span class="text-cus-primary">JUNE & DECEMBER</span>',
          items: [
            {
              title: 'Communication and Language',
              lists: [
                'English',
                'Myanmar'
              ]
            },
            {
              title: 'Litercy',
              lists: [
                'English & Myanmar',
                'English Phonics',
              ]
            },
            {
              title: 'Personal, Social, Health & Emotional Development',
              lists: [
                'Life Skills',
                'Personal Hygiene',
                'Myanmar Short Stories for Moral Value',
              ]
            },
            {
              title: 'Physical Development',
              lists: [
                'Fine & Gross Motor Skills',
                'Music & Movement',
                'Yoga',
              ]
            },
            {
              title: 'Numeracy/ Mathematics',
              lists: null
            },
            {
              title: 'STEAM(Science, Technology, Engineering, Art & Maths)',
              lists: null
            },
            {
              title: 'Mindfulness',
              lists: null
            },
            {
              title: 'Montessori Education',
              lists: null
            },
            {
              title: 'Digital Learning for Skill Enhacement',
              lists: [
                'Maths',
                'English'
              ]
            },
          ]
        },
        {
          id: 'Nusery2',
          title: 'NUSERY 2',
          subtitle: '<span class="text-cus-secondary">INTAKE</span> - <span class="text-cus-primary">JUNE & DECEMBER</span>',
          items: [
            {
              title: 'Communication and Language',
              lists: [
                'English',
                'Myanmar'
              ]
            },
            {
              title: 'Litercy',
              lists: [
                'English & Myanmar',
                'English Phonics',
              ]
            },
            {
              title: 'Personal, Social, Health & Emotional Development',
              lists: [
                'Life Skills',
                'Personal Hygiene',
                'Myanmar Short Stories for Moral Value',
              ]
            },
            {
              title: 'Physical Development',
              lists: [
                'Fine & Gross Motor Skills',
                'Music & Movement',
                'Yoga',
              ]
            },
            {
              title: 'Numeracy/ Mathematics',
              lists: null
            },
            {
              title: 'STEAM(Science, Technology, Engineering, Art & Maths)',
              lists: null
            },
            {
              title: 'Mindfulness',
              lists: null
            },
            {
              title: 'Montessori Education',
              lists: null
            },
            {
              title: 'Digital Learning for Skill Enhacement',
              lists: [
                'Maths',
                'English'
              ]
            },
          ]
        },
        {
          id: 'prekg1',
          title: 'PRE-KG 1',
          subtitle: '<span class="text-cus-secondary">INTAKE</span> - <span class="text-cus-primary">JUNE & DECEMBER</span>',
          items: [
            {
              title: 'Communication and Language',
              lists: [
                'English',
                'Myanmar'
              ]
            },
            {
              title: 'Litercy',
              lists: [
                'English & Myanmar',
                'English Phonics',
              ]
            },
            {
              title: 'Personal, Social, Health & Emotional Development',
              lists: [
                'Life Skills',
                'Personal Hygiene',
                'Myanmar Short Stories for Moral Value',
              ]
            },
            {
              title: 'Physical Development',
              lists: [
                'Fine & Gross Motor Skills',
                'Music & Movement',
                'Yoga',
              ]
            },
            {
              title: 'Numeracy/ Mathematics',
              lists: null
            },
            {
              title: 'STEAM(Science, Technology, Engineering, Art & Maths)',
              lists: null
            },
            {
              title: 'Mindfulness',
              lists: null
            },
            {
              title: 'Montessori Education',
              lists: null
            },
            {
              title: 'Digital Learning for Skill Enhacement',
              lists: [
                'Maths',
                'English'
              ]
            },
          ]
        },
        {
          id: 'prekg2',
          title: 'PRE-KG 2',
          subtitle: '<span class="text-cus-secondary">INTAKE</span> - <span class="text-cus-primary">JUNE & DECEMBER</span>',
          items: [
            {
              title: 'Communication and Language',
              lists: [
                'English',
                'Myanmar'
              ]
            },
            {
              title: 'Litercy',
              lists: [
                'English & Myanmar',
                'English Phonics',
              ]
            },
            {
              title: 'Personal, Social, Health & Emotional Development',
              lists: [
                'Life Skills',
                'Personal Hygiene',
                'Myanmar Short Stories for Moral Value',
              ]
            },
            {
              title: 'Physical Development',
              lists: [
                'Fine & Gross Motor Skills',
                'Music & Movement',
                'Yoga',
              ]
            },
            {
              title: 'Numeracy/ Mathematics',
              lists: null
            },
            {
              title: 'STEAM(Science, Technology, Engineering, Art & Maths)',
              lists: null
            },
            {
              title: 'Mindfulness',
              lists: null
            },
            {
              title: 'Montessori Education',
              lists: null
            },
            {
              title: 'Digital Learning for Skill Enhacement',
              lists: [
                'Maths',
                'English'
              ]
            },
          ]
        },
        {
          id: 'prekg3',
          title: 'PRE-KG 3',
          subtitle: '<span class="text-cus-secondary">INTAKE</span> - <span class="text-cus-primary">JUNE & DECEMBER</span>',
          items: [
            {
              title: 'Communication and Language',
              lists: [
                'English',
                'Myanmar'
              ]
            },
            {
              title: 'Litercy',
              lists: [
                'English & Myanmar',
                'English Phonics',
              ]
            },
            {
              title: 'Personal, Social, Health & Emotional Development',
              lists: [
                'Life Skills',
                'Personal Hygiene',
                'Myanmar Short Stories for Moral Value',
              ]
            },
            {
              title: 'Physical Development',
              lists: [
                'Fine & Gross Motor Skills',
                'Music & Movement',
                'Yoga',
              ]
            },
            {
              title: 'Numeracy/ Mathematics',
              lists: null
            },
            {
              title: 'STEAM(Science, Technology, Engineering, Art & Maths)',
              lists: null
            },
            {
              title: 'Mindfulness',
              lists: null
            },
            {
              title: 'Montessori Education',
              lists: null
            },
            {
              title: 'Digital Learning for Skill Enhacement',
              lists: [
                'Maths',
                'English'
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