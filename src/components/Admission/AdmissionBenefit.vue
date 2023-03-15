<template>
  <div class="text-start mb-5">
    <h2 class="title text-uppercase mb-3">Benefits of an smk education</h2>
    <p class="benefit-content">
      Lorem ipsum dolor sit amet consectetur adipisicing elit. Ipsam libero accusamus harum velit, praesentium porro
      blanditiis sed, ex iure neque iste! Similique quaerat blanditiis ratione culpa minus dicta optio facere? Lorem ipsum
      dolor sit amet consectetur adipisicing elit. Ipsam libero accusamus harum velit, praesentium porro blanditiis sed,
      ex iure neque iste! Similique quaerat blanditiis ratione culpa minus dicta optio facere?
      Lorem ipsum dolor sit amet consectetur adipisicing elit. Ipsam libero accusamus harum velit, praesentium porro
      blanditiis sed, ex iure neque iste! Similique quaerat blanditiis ratione culpa minus dicta optio facere?Lorem ipsum
      dolor sit amet consectetur adipisicing elit. Ipsam libero accusamus harum velit, praesentium porro blanditiis sed,
      ex iure neque iste! Similique quaerat blanditiis ratione culpa minus dicta optio facere?
      Lorem ipsum dolor sit amet consectetur adipisicing elit. Ipsam libero accusamus harum velit, praesentium porro
      blanditiis sed, ex iure neque iste! Similique quaerat blanditiis ratione culpa minus dicta optio facere?
    </p>
  </div>

  <div class="row">
      <AdmissionLinkCard v-for="card in benefitCards" :key="card.id" :card="card" class="col-3">
      </AdmissionLinkCard>
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
      benefitCards: [
        { id: 0, title: 'required documentation', class: 'image-1', url: 'RequiredDocumentation' },
        { id: 0, title: 'fees', class: 'image-2', url: 'Fees' },
        { id: 0, title: 'faq', class: 'image-3', url: 'Fees' },
        { id: 0, title: 'waitlist form', class: 'image-4', url: 'waitinglist' },
      ]
    }
  },
}
</script>

<style lang="scss" scoped>
.title {
  color: var(--cus-secondary-bold);
  font-weight: var(--cus-fw-semibold);
  text-align: left;
}

.benefit-content {
  line-height: 30px;
}
</style>