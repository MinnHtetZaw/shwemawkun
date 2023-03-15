<template>
  <div class="text-start">
    <h2 class="title text-uppercase mb-5">Admission Timeline</h2>
    <AdmissionStepRow v-for="row in rows" :row="row" :key="row.id" class="mb-5"></AdmissionStepRow>
  </div>
</template>

<script>
import AdmissionStepRow from "@/components/Admission/AdmissionStepRow.vue";
export default {
  components: {
    AdmissionStepRow,
  },
  data() {
    return {
      rows: [
        {
          id: 1,
          title: 'pre-school (early years)',
          stepCards: [
            { id: 1, description: "Review online application form", img: "image-11" },
            { id: 2, description: "Admission Notification Begin", img: "image-12" },
            { id: 3, description: "Admission Notification for Assessment", img: "image-13" },
            { id: 4, description: "Parent Interveiw and Class Allocation", img: "image-14" },
            { id: 5, description: "Re-enrollment<br/><span class='fw-normal'>(Current Families)</span>", img: "image-15" },
            { id: 6, description: "Orientation / <br/>Terms Begin", img: "image-16" },
          ],
        },
        {
          id: 2,
          title: 'primary & secondary',
          stepCards: [
            { id: 1, description: "Enrollment Notification Begin", img: "image-21" },
            {
              id: 2,
              description: "Re-enrollment<br/><span class='fw-normal'>(Current Pre-school Students for KG)</span>",
              img: "image-22"
            },
            {
              id: 3,
              description: "Primary & Secondary Re-enrollment<br/><span class='fw-normal'>(Current Students)</span>",
              img: "image-23"
            },
            {
              id: 4,
              description: "Review Waitlist<br/><span class='fw-normal'>(New Primary & Secondary Students)</span>",
              img: "image-24"
            },
            {
              id: 5,
              description: "Plaement Test Conducted and Enrollment Process Begin<br/><span class='fw-normal'>(New Primary & Secondary Students)</span>",
              img: "image-25"
            },
            {
              id: 6,
              description: "Orientation",
              img: "image-26"
            },
            { id: 7, description: "Academic Year Begin", img: "image-27" },
          ],
        },
        {
          id: 3,
          title: 'weekend class',
          stepCards: [
            {
              id: 1,
              description: "Re-enrollment Notification Begin<br/><span class='fw-normal>(Summer & Weekday Students)</span>",
              img: "image-31"
            },
            {
              id: 2,
              description: "Review Waillist and Palcement Test Notification<br/><span class='fw-normal'>(New Students)</span>",
              img: "image-32"
            },
            { id: 3, description: "Placement Test Conducted", img: "image-33" },
            { id: 4, description: "Programme Enrollment", img: "image-34" },
            { id: 5, description: "Orientation", img: "image-35" },
            { id: 6, description: "Programme Begin", img: "image-36" },
          ],
        },
        {
          id: 4,
          title: 'summer class',
          stepCards: [
            {
              id: 1,
              description: "Re-enrollment Notification Begin<br/><span class='fw-normal>(Summer & Weekday Students)</span>",
              img: "image-41"
            },
            {
              id: 2,
              description: "Review Waillist and Palcement Test Notification<br/><span class='fw-normal'>(New Students)</span>",
              img: "image-42"
            },
            { id: 3, description: "Placement Test Conducted", img: "image-43" },
            { id: 4, description: "Programme Enrollment", img: "image-44" },
            { id: 5, description: "Orientation", img: "image-45" },
            { id: 6, description: "Programme Begin", img: "image-46" },
          ],
        },
      ]
    };
  },
};
</script>

<style lang="scss" scoped>
.title {
  color: var(--cus-secondary-bold);
  font-size: var(--cus-fs-xxx-large);
  font-weight: var(--cus-fw-semibold);
  text-align: left;
}
</style>
