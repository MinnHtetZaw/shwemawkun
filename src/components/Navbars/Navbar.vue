<template>
  <nav class="navbar navbar-expand-lg nav_in navbar-dark">
    <button class="navbar-toggler" type="button" @click="navshow()" data-bs-toggle="collapse"
      data-bs-target="#navbarNavDropdown" aria-controls="navbarNavDropdown" aria-expanded="false"
      aria-label="Toggle navigation">
      <span class="navbar-toggler-icon"></span>
    </button>
    <div class="collapse navbar-collapse justify-content-center" id="navbarNavDropdown">
      <ul class="navbar-nav" style="margin-left:50px">
        <li class="nav-item mb-2 mt-2">
          <router-link :to="{ name: 'Home', params: { schtype: schtype } }" class="cus_nav" aria-current="page">
            <span v-if="font_type == 1">Home</span>
            <span v-if="font_type == 2">မူလစာမျက်နှာ</span>
          </router-link>
        </li>
        <li class="nav-item mb-2 mt-2">
          <router-link :to="{ name: 'AboutSchool' }" class="nav-link cus_nav">
            <span v-if="font_type == 1">About us</span>
            <span v-if="font_type == 2">ကျောင်း</span>
          </router-link>
        </li>
        <li class="nav-item mb-2 mt-2">
          <div @click="$emit('openAcademicBar')" class="nav-link cus_nav hover-cursor">
            <span v-if="font_type == 1">Academic</span>
            <span v-if="font_type == 2">ပညာရေး</span>
          </div>
        </li>
        <li class="nav-item mb-2 mt-2">
          <div @click="$emit('openSubNavbar')" class="nav-link cus_nav hover-cursor">
            <span v-if="font_type == 1">Admission</span>
            <span v-if="font_type == 2">၀င်ခွင့်</span>
          </div>
        </li>
        <li class="nav-item mb-2 mt-2">
          <router-link :to="{ name: 'Career' }" class="nav-link cus_nav">
            <span v-if="font_type == 1">Career</span>
            <span v-if="font_type == 2">စည်းကမ်းများ</span>
          </router-link>
        </li>
        <li class="nav-item mb-2 mt-2">
          <router-link :to="{ name: 'Contactus' }" class="nav-link cus_nav">
            <span v-if="font_type == 1">Contact us</span>
            <span v-if="font_type == 2">အခြား</span>
          </router-link>
        </li>
      </ul>
    </div>
  </nav>
</template>

<script>
export default {
  props: ['schtype', 'font_type']
}
</script>

<style lang="scss" scoped></style>