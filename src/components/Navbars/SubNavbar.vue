<template>
  <nav class="cus_sub_nav navbar navbar-expand-lg navbar-light">
    <div class="container">
      <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNav"
        aria-controls="navbarNav" aria-expanded="false" aria-label="Toggle navigation">
        <span class="navbar-toggler-icon"></span>
      </button>
      <div class="collapse navbar-collapse justify-content-center w-100" id="navbarNav">
        <ul class="navbar-nav justify-content-between">
          <li class="nav-item mb-2 mt-2">
            <router-link :to="{ name: 'AdmissionOverview' }" class="nav-link" :class="{'fw-bold': isActiveLink('AdmissionOverview')}">
              <span v-if="font_type == 1">Admission Overview</span>
              <span v-if="font_type == 2">ကျောင်း</span>
            </router-link>
          </li>
          <li class="nav-item mb-2 mt-2">
            <router-link :to="{ name: 'RequiredDocumentation' }" class="nav-link" :class="{ 'fw-bold': isActiveLink('RequiredDocumentation') }">
              <span v-if="font_type == 1">Required Documentation</span>
              <span v-if="font_type == 2">ကျောင်း</span>
            </router-link>
          </li>
          <li class="nav-item mb-2 mt-2">
            <router-link :to="{ name: 'Fees' }" class="nav-link" :class="{ 'fw-bold': isActiveLink('Fees') }">
              <span v-if="font_type == 1">Fees</span>
              <span v-if="font_type == 2">ကျောင်း</span>
            </router-link>
          </li>
          <li class="nav-item mb-2 mt-2">
            <router-link :to="{ name: 'AboutUs' }" class="nav-link" :class="{ 'fw-bold': isActiveLink('AboutUs') }">
              <span v-if="font_type == 1">FAQ</span>
              <span v-if="font_type == 2">ကျောင်း</span>
            </router-link>
          </li>
          <li class="nav-item mb-2 mt-2">
            <router-link :to="{ name: 'waitinglist' }" class="nav-link" :class="{ 'fw-bold': isActiveLink('waitinglist') }">
              <span v-if="font_type == 1">Waitlist Form</span>
              <span v-if="font_type == 2">ကျောင်း</span>
            </router-link>
          </li>
        </ul>
      </div>
    </div>
  </nav>
</template>

<script>
export default {
  props: {
    font_type: {
      type: Number,
      default: 1,
    }
  },
  methods: {
    isActiveLink(name) {
      return this.$route.name === name
    }
  }
}
</script>

<style lang="scss" scoped></style>