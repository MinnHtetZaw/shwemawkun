<template>
  <div class="text-start">
    <div class="container push-up-6">
      <section>
        <h1 class="title text-uppercase mb-5">required documentation</h1>
        <div class="list-box">
          <div class="list-title p-4">Lorem ipsum dolor sit amet consectetur adipisicing elit.</div>
          <div class="lists">
            <div v-for="n in 10" class="px-5 py-3">Lorem ipsum dolor sit amet consectetur adipisicing elit. Ducimus nulla
              minus, voluptas sed voluptatem ipsam
              est</div>
          </div>
        </div>
      </section>
      <section class="push-y-6">
        <h1 class="title sub-title text-uppercase mb-5">next what</h1>
        <div class="row text-center">
          <AdmissionLinkCard v-for="card in nextWhatCards" :key="card.id" :card="card" class="col-4">
          </AdmissionLinkCard>
        </div>
      </section>
    </div>
  </div>
</template>

<script>
import AdmissionLinkCard from '@/components/Admission/AdmissionLinkCard.vue'
export default {
  components: {
    AdmissionLinkCard,
  },
  data() {
    return {
      nextWhatCards: [
        { id: 0, title: 'required documentation', class: 'image-1', url: 'RequiredDocumentation' },
        { id: 0, title: 'fees', class: 'image-2', url: 'Fees' },
        { id: 0, title: 'faq', class: 'image-3', url: 'Fees' },
      ]
    }
  }
}
</script>

<style lang="scss" scoped>
.title {
  letter-spacing: 5px;
  font-weight: var(--cus-fw-semibold);
  color: var(--cus-secondary);
}

.sub-title {
  color: var(--cus-primary)
}

.list-title {
  text-transform: uppercase;
  font-weight: var(--cus-fw-semibold);
  font-size: var(--cus-fs-xx-large);
  color: var(--cus-white);
  background-color: var(--cus-primary);
}

.list-box {
  border: 1px solid var(--cus-dark)
}

.lists {
  div {
    font-size: var(--fs-xx-large);
  }

  div:not(:last-child) {
    border-bottom: 1px solid var(--cus-dark);
  }
}

.push-up-6 {
  margin-top: 6rem;
}

.push-y-6 {
  margin: 6rem 0;
}
</style>