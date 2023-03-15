<script>
import HoverableDropdown from '@/components/HoverableDropdown.vue'
export default {
  components: {
    HoverableDropdown,
  },
  props: {
    font_type: {
      type: Number,
      default: 1,
    }
  },

  data() {
    return {
      routes: {
        "weekday": [
          { name: 'Pre-school(Early years)', to: 'AcademicWeekdayPreSchool' },
          { name: 'Primary', to: 'AcademicWeekdayPrimary' },
          { name: 'Secondary', to: 'AcademicWeekdaySecondary' },
        ],
        "weekend": [
          { name: 'Pre-school(Early years)', to: 'AcademicWeekendPreSchool' },
          { name: 'International Primary', to: 'AcademicWeekendPrimary' },
          { name: 'International Secondary', to: 'AcademicWeekendSecondary' },
        ]
      }
    }
  },
  methods: {
    isActiveLink(name) {
      return this.$route.name === name
    }
  }
}
</script>

<template>
  <nav class="navbar academic-nav navbar-expand-lg navbar-light border-bottom">
    <div class="container">
      <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNav"
        aria-controls="navbarNav" aria-expanded="false" aria-label="Toggle navigation">
        <span class="navbar-toggler-icon"></span>
      </button>
      <div class="collapse navbar-collapse justify-content-center w-100" id="navbarNav">
        <ul class="navbar-nav justify-content-between align-items-center">
          <li class="nav-item">
            <HoverableDropdown :routes="routes.weekday">Weekday classes</HoverableDropdown>
          </li>
          <li class="nav-item">
            <HoverableDropdown :routes="routes.weekend">weekend classes & summer programme</HoverableDropdown>
          </li>
        </ul>
      </div>
    </div>
  </nav>
</template>

<style lang="scss" scoped>
.navbar {
  background-color: white;
  border: 0;
  padding-top: 0;
  padding-bottom: 0;

  .nav-item {
    color: var(--cus-primary);
    font-weight: var(--cus-fw-semibold) !important;
    padding: 0;
    font-weight: var(--cus-fw-semibold) !important;
    color: var(--cus-primary);

    &.active {
      color: var(--cus-white) !important;
      background-color: var(--cus-primary);

      & .router-link-exact-active {
        color: var(--cus-white);
      }

      .dropdown-toggle {
        color: var(--cus-white) !important;
      }
    }
  }

  .nav-link {
    padding: 10px 20px;
  }
}

.cus-dropdown-link {
  &:hover~.cus-dropdown-menu {
    display: block;
  }
}

.cus-toggle-btn {
  border: 0;
  border-radius: 0;
  padding: 8px;
}

.cus-dropdown-menu {
  display: none;
  padding: 5px;
  left: -20px;
  top: 48px;
  background-color: aliceblue;

  .dropdown-item {
    color: var(--cus-primary) !important;

    &.active {
      color: var(--cus-white) !important;
      background-color: var(--cus-primary);
    }
  }
}
</style>