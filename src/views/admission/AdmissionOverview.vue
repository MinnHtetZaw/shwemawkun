<template>
  <div>
    <!-- admission overview section -->
    <div class="admission_overview">
      <div class="container mx-auto py-5">
        <section class="mb-5">
          <AdmissionOverviewCard></AdmissionOverviewCard>
        </section>
        <section class="mb-5">
          <AdmissionTimeline></AdmissionTimeline>
        </section>
        <section>
          <AdmissionBenefit></AdmissionBenefit>
        </section>
      </div>
    </div>
  </div>
</template>

<script>
import AdmissionOverviewCard from '@/components/Admission/AdmissionOverviewCard.vue'
import AdmissionTimeline from '@/components/Admission/AdmissionTimiline.vue'
import AdmissionBenefit from '@/components/Admission/AdmissionBenefit.vue'
export default {
  components: {
    AdmissionOverviewCard,
    AdmissionTimeline,
    AdmissionBenefit,
  }
}
</script>

<style lang="scss" scoped>
</style>