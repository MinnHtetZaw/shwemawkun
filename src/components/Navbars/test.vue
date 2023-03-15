<template>
  <nav class="navbar navbar-expand-lg navbar-light py-2">
    <div class="container">
      <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNav"
        aria-controls="navbarNav" aria-expanded="false" aria-label="Toggle navigation">
        <span class="navbar-toggler-icon"></span>
      </button>
      <div class="collapse navbar-collapse justify-content-center w-100" id="navbarNav">
        <ul class="navbar-nav justify-content-between">
          <li class="nav-item">
            <div class="btn-group">
              <button type="button" class="btn cus-toggle-btn dropdown-toggle" data-bs-toggle="dropdown"
                aria-expanded="false">
                Action
              </button>
              <ul class="dropdown-menu">
                <li>
                  <router-link :to="{ name: 'AcademicPreSchool' }" class="nav-link"
                    :class="{ 'bg-cus-primary text-white': isActiveLink('RequiredDocumentation') }">
                    <span v-if="font_type == 1">Required Documentation</span>
                    <span v-if="font_type == 2">ကျောင်း</span>
                  </router-link>
                </li>
                <li><a class="dropdown-item" href="#">Another action</a></li>
                <li><a class="dropdown-item" href="#">Something else here</a></li>
              </ul>
            </div>
          </li>
          <li class="nav-item">
            <router-link :to="{ name: 'RequiredDocumentation' }" class="nav-link"
              :class="{ 'bg-cus-primary text-white': isActiveLink('RequiredDocumentation') }">
              <span v-if="font_type == 1">Required Documentation</span>
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

<style lang="scss" scoped>
.navbar {
  background-color: white;
  border: 0;

  li a {
    color: var(--cus-primary);
    font-weight: normal;
  }
}

.cus-toggle-btn {
  border: 0;
  border-radius: 0;
}
</style>