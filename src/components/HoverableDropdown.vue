<template>
  <div class="dropdown">
    <button class="dropbtn">
      <slot></slot>
    </button>
    <div class="dropdown-content">
      <router-link v-for="route in routes" :to="{ name: route.to }">{{ route.name }}</router-link>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    routes: Array
  }
}
</script>

<style lang="scss" scoped>
/* Dropdown Button */
.dropbtn {
  color: var(--cus-primary);
  background-color: var(--cus-white);
  font-size: 16px;
  padding: 10px 20px;
  border: none;
  text-transform: capitalize;
}

/* The container <div> - needed to position the dropdown content */
.dropdown {
  position: relative;
  display: inline-block;
}

/* Dropdown Content (Hidden by Default) */
.dropdown-content {
  display: none;
  position: absolute;
  background-color: #f1f1f1;
  min-width: 160px;
  width: 240px;
  box-shadow: 0px 8px 16px 0px rgba(0, 0, 0, 0.2);
  z-index: 1;
}

/* Links inside the dropdown */
.dropdown-content a {
  color: black;
  padding: 12px 16px;
  text-decoration: none;
  display: block;
}

/* Change color of dropdown links on hover */
.dropdown-content a:hover {
  background-color: #ddd;
}

/* Show the dropdown menu on hover */
.dropdown:hover .dropdown-content {
  display: block;
}

/* Change the background color of the dropdown button when the dropdown content is shown */
.dropdown:hover .dropbtn {
  background-color: var(--cus-primary);
  color: var(--cus-white);
}
</style>