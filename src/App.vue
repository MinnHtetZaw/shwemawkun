<script>

import $ from "jquery";

import "../node_modules/jquery/dist/jquery.min.js";
import "../node_modules/jquery/dist/jquery.js";
import "@fortawesome/free-solid-svg-icons"

import Navbar from '@/components/Navbars/Navbar.vue'
import SubNavbar from '@/components/Navbars/SubNavbar.vue'
import AcademicBar from "./components/Navbars/AcademicBar.vue";

export default {
  components: {
    Navbar,
    SubNavbar,
    AcademicBar
  },
  data() {
    return {
      path: false,
      schtype: "",
      font_type: 1,
      path1: null,
      isSubNavbarOpen: false,
      isAcademicBarOpen: false,
      navOpened: false
    };
  },


  mounted() {
    if (localStorage.getItem("font_type")) {
      this.font_type = localStorage.getItem("font_type")
    }
    else {
      localStorage.setItem("font_type", 2);
    }
    // alert(localStorage.getItem("font_type"));
  },
  methods: {
    font_change: function () {
      localStorage.setItem("font_type", this.font_type);
    },
    closeSubNavbars: function () {
      this.isSubNavbarOpen = false;
      this.isAcademicBarOpen = false;
    },
    toggleAcademicBar: function () {
      if (this.isSubNavbarOpen) {
        this.isSubNavbarOpen = false
      }
      this.isAcademicBarOpen = !this.isAcademicBarOpen;
    },
    toggleSubNavbar: function () {
      if (this.isAcademicBarOpen) {
        this.isAcademicBarOpen = false
      }
      this.isSubNavbarOpen = !this.isSubNavbarOpen;
    }
  },
  created() { },
  watch: {
    $route(to, from) {
      var currentUrl = window.location.pathname;
      var Url = currentUrl.split("/");
      if (window.location.pathname.split("/")[1] == '') {
        this.path1 = true;
      } else {
        this.path1 = false;
      }
      //  alert(currentUrl);
      if (Url[1] == "Admin") {
        this.path = true;
      } else {
        this.path = false;
      }

      // $(window).ready(function () {
      //   $("#see").show();
      //   $("#hide").hide();

      //   setTimeout(function () {
      //     $("#hide").show();
      //     $("#see").hide();
      //   }, 3000);
      // });
    },
  },
};
</script>

<template>
  <div class="nav_all ">
    <div class="nav_shade">
      <nav class="navbar navbar-expand-lg bg-light">
        <div class="container-fluid">
          <a class="navbar-brand" style="margin-left:50px" href="#">
            <div class="row">
              <div class="col">
                <img class="navlogo" src="./assets/img/logo.png" alt="" />
              </div>
              <div class="col">
                <router-link :to="{ name: 'Home', params: { userId: 1 } }" class="nav-link" aria-current="page">
                  <img src="./assets/img/navlogo.png" style="width:150px" alt="">
                </router-link>
              </div>
            </div>
          </a>
          <a class="navbar-brand ms-auto" href="#">
            <div class="row">

              <div class="col">

                <select name="" class="form-control rounded-pill text-center" v-model="font_type" @change="font_change"
                  style="border-color: purple;" id="">
                  <option value="1"
                    style="background-image: url('./assets/img/myanmarflag.png');  background-repeat: no-repeat;background-attachment: fixed;background-position: center;">
                    English Language</option>
                  <option value="2">Myanmar Language</option>
                </select>
                <h5 class="mt-2">

                  <font-awesome-icon class="m-1" style="width:35px; height: 35px;  color:purple;"
                    icon="fa-brands fa-facebook" />
                  <font-awesome-icon class="m-1"
                    style="width:19px; height: 19px;  color:white; border:0px; border-style: solid; border-radius: 40px;  background-color: purple; padding:8px"
                    icon="fa-brands fa-instagram" />
                  <font-awesome-icon class="m-1"
                    style="width:19px; height: 19px;  color:white; border:0px; border-style: solid; border-radius: 40px;  background-color: purple; padding:8px"
                    icon="fa-brands fa-linkedin" />
                  <font-awesome-icon class="m-1"
                    style="width:19px; height: 19px;  color:white; border:0px; border-style: solid; border-radius: 40px;  background-color: purple; padding:8px"
                    icon="fa-brands fa-whatsapp" />
                  <font-awesome-icon class="m-1"
                    style="width:19px; height: 19px;  color:white; border:0px; border-style: solid; border-radius: 40px;  background-color: purple; padding:8px"
                    icon="fa-brands fa-youtube" />
                  <font-awesome-icon class="m-1"
                    style="width:35px; height: 35px;  color:purple; border:0px; border-style: solid; border-radius: 40px;  background-color: white; "
                    icon="fa-brands fa-telegram" />
                </h5>
              </div>
          </div>
        </a>
        </div>
      </nav>
    </div>
  </div>

  <div v-if="!path" class="sticky-top">
    <!-- purple nav -->
    <Navbar @openSubNavbar="toggleSubNavbar" @openAcademicBar="toggleAcademicBar" :font_type="font_type"
      :schtype="schtype"></Navbar>

    <!-- gold nav -->
    <template v-if="isSubNavbarOpen">
      <SubNavbar :font_type="font_type"></SubNavbar>
    </template>

    <template v-if="isAcademicBarOpen">
      <AcademicBar :font_type="font_type"></AcademicBar>
    </template>
  </div>

  <div v-if="path">
    <div class="nav_all ">
      <div class="nav_shade">
        <nav class="navbar navbar-expand-lg nav_in ">
          <div class="container-fluid">

            <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNavDropdown"
              aria-controls="navbarNavDropdown" aria-expanded="false" aria-label="Toggle navigation">
              <span class="navbar-toggler-icon"></span>
            </button>
            <div class="collapse navbar-collapse" id="navbarNavDropdown">
              <ul class="navbar-nav" style="margin-left:50px">
                <li class="nav-item mt-3 mb-2">
                  <router-link :to="{ name: 'waitinglistview', params: { userId: 3 } }" class="cus_nav">Waiting List <span
                      class="nav_hidden_text">View</span>
                  </router-link>
                </li>
                <li class="nav-item mt-3 mb-2">
                  <router-link :to="{ name: 'eventregister', params: { userId: 3 } }" class="cus_nav">Event <span
                      class="nav_hidden_text">Register</span>
                  </router-link>
                </li>

                <li class="nav-item mt-3 mb-2">
                  <router-link :to="{ name: 'ContactusView', params: { userId: 3 } }" class="cus_nav">Contactus <span
                      class="nav_hidden_text">View</span>
                  </router-link>
                </li>

                <li class="nav-item mt-3 mb-2">
                  <router-link :to="{ name: 'calendar', params: { userId: 3 } }" class="cus_nav">Calendar <span
                      class="nav_hidden_text">Register</span>
                  </router-link>
                </li>

                <li class="nav-item mt-3 mb-2">
                  <router-link :to="{ name: 'FeesRegister', params: { userId: 3 } }" class="cus_nav">Fees <span
                      class="nav_hidden_text">Register</span>
                  </router-link>
                </li>

                <li class="nav-item mt-3 mb-2">
                  <router-link :to="{ name: 'CoursesRegister', params: { userId: 3 } }" class="cus_nav">Course
                    <span class="nav_hidden_text">Register</span></router-link>
                </li>

                <li class="nav-item mt-3 mb-2">
                  <router-link :to="{ name: 'CareerView', params: { userId: 3 } }" class="cus_nav">Career
                    <span class="nav_hidden_text">View</span></router-link>
                </li>

                <li class="nav-item mt-3 mb-2">
                  <router-link :to="{ name: 'TeacherRegister', params: { userId: 3 } }" class="cus_nav">Teacher <span
                      class="nav_hidden_text">Register</span>
                  </router-link>
                </li>
                <li class="nav-item mt-3 mb-2">
                  <router-link :to="{ name: 'logout', params: { userId: 3 } }"
                    class="btn btn-success">Logout</router-link>
                </li>
              </ul>
            </div>
          </div>
        </nav>
      </div>
    </div>
  </div>

  <!-- loading photo -->
  <!-- <div id="see">
        <img class="loaderphoto" src="./assets/img/smkloading.gif" alt="" />
      </div> -->
  <!-- loading photo -->

  <!--  #f3cd5d -->
  <div id="hide" style="background-color: #FFFFFF">
    <router-view />
  </div>

  <footer>
    <div class="Part7">
      <div class="footer">
        <div class=" footer_div">
          <div class="cus-container py-3">
            <div class="row gx-0 gy-3 justify-content-center">

              <div class="col-sm-4 bd_footer">
                <div>
                  <h1 class="text-start text-uppercase" style="font-size:25px;font-weight:900">Shwe Maw Kun</h1>
                  <p class="text-start mb-1 fw-normal text-white">About Us</p>
                  <p class="text-start mb-1 fw-normal text-white">Distribution and Manufacturing</p>
                  <p class="text-start mb-1 fw-normal text-white">Our Purpose</p>
                  <p class="text-start mb-1 fw-normal text-white">Our Vision and Mission</p>
                  <p class="text-start mb-1 fw-normal text-white">Our Culture</p>
                  <p class="text-start mb-1 fw-normal text-white">CSR Activities</p>

                </div>

              </div>
              <div class="col-sm-4 bd_footer">
                <i class="bi bi-geo-alt icon"></i>
                <div style="padding-left: 65px;">
                  <h1 class="text-uppercase text-start" style="font-size:25px;font-weight:900">{{ font_type == 1 ?
                    "Contact Us" : "ဆက်သွယ်ရန်ဖုန်းနံပတ်များ" }}</h1>
                  <p class="mb-1 fw-normal text-start">{{ font_type == 1 ? "09 123 456 789" : "၀၉ ၁၂၃ ၄၅၆ ၇၈၉" }}</p>
                  <p class="mb-1 fw-normal text-start">{{ font_type == 1 ? "09 987 343 565" : "၀၉ ၉၈၇ ၃၄၃ ၅၆၅" }}</p>

                </div>
              </div>
              <!-- here -->
              <div class="col-sm-4 footer-links bd_footer">
                <div class="d-flex justify-content-center social-links footer_cent">
                  <div style="padding-right: 65px;">
                    <h1 class="text-uppercase text-start" style="font-size:25px;font-weight:900;">{{ font_type == 1 ? "Address" : "ဆက်သွယ်ရန်လိပ်စာ" }}</h1>
                    <p class="mb-1 fw-normal text-start">
                      {{ font_type == 1 ? 'No. 20/10,Shwe Chi Street, (Corner of Yae Htwet Oo Street),Yae Aye Kwin Quarter, Taunggyi, Shan State, Myanmar' : ' အမှတ်(၂၀/၁၀)၊ရွှေချည်လမ်း နှင့် ရေထွက်ဦး လမ်းထောင့်၊ ရေအေးကွင်းရပ်၊ တောင်ကြီးမြို့။' }}
                      <br />
                    </p>
                  </div>
                </div>
              </div>
              <!-- here -->
            </div>
          </div>
        </div>
      </div>

      <div class="row" v-if="path1 == true">
        <div class="col-md-4 ">
          <div style="width:100%;height:400px;" class="">
            <img src="./assets/img/footerlogo1.jpg" class="footer-logo-img" alt="">
          </div>
        </div>
        <div class="col-md-4 ">
          <div style="width:100%;height:400px;" class="">
            <img src="./assets/img/footerlogo2.jpg" class="footer-logo-img" alt="">
          </div>
        </div>
        <div class="col-md-4 ">
          <div style="width:100%;height:400px;" class="">
            <img src="./assets/img/footerlogo3.jpg" class="footer-logo-img" alt="">
          </div>
        </div>

      </div>
    </div>
  </footer>
</template>

<style lang="scss">
html,
* {
  font-family: 'Golos Text', sans-serif;
}

:root {
  --cus-primary: #7f3874;
  --cus-secondary: #f2bc00;
  --cus-secondary-bold: #db9000;
  --cus-secondary-bold-2: #db3e00;
  --cus-dark: #000000;
  --cus-white: #ffffff;
  --cus-grey: #e3e1e2;

  // font size
  --cus-fs-normal: 16px;
  --cus-fs-large: 20px;
  --cus-fs-x-large: 24px;
  --cus-fs-xx-large: 28px;
  --cus-fs-xxx-large: 32px;
  --cus-fs-xxxx-large: 38px;

  // font weight 
  --cus-fw-semibold: 600;

  // border radisu
  --cus-border-radius: 15px;
}

// helpers
.hover-cursor {
  cursor: pointer;
}

.bg-cus-primary {
  background-color: var(--cus-primary)
}

.bg-cus-secondary {
  background-color: var(--cus-secondary);
}

.text-cus-primary {
  color: var(--cus-primary)
}

.text-cus-secondary {
  color: var(--cus-secondary);
}

.cus-container {
  max-width: 1082px;
  margin-left: auto;
  margin-right: auto;
}

// helpers end

.loaderphoto {
  margin: 20vh;
  width: 300px;

  z-index: 200;
  border: 0px;
  border-style: none;
  border-radius: 50%;
  box-shadow: 0px 0px 8px 2px rgba(0, 0, 0, 0.75);
  -webkit-box-shadow: 0px 0px 8px 2px rgba(0, 0, 0, 0.75);
  -moz-box-shadow: 0px 0px 8px 2px rgba(0, 0, 0, 0.75);
}

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

nav {
  padding: 30px;
  background-color: var(--cus-primary);

  a {
    font-size: 17px;
    color: #ffffff;

    &.router-link-exact-active {
      color: gold;
    }
  }
}

.cus_nav {
  display: inline-block;
  padding: 5px 8px;
  width: 120px;
  margin-right: 3.5vw;
  text-decoration: none;
  border: 0px;
  font-size: 20px;
  color: #ffffff;
  // border-bottom: 1px;
  border-style: solid;
  border-radius: 5px;
  transition: 0.5s;
}

.cus_nav:hover {
  // padding: 10px;
  animation-name: color;
  animation-duration: 1s;
  color: purple;
  background-color: rgb(255, 255, 255);
  // box-shadow: 1px 3px 3px blue;
  // backdrop-filter: blur(10px);
}

.cus_nav:hover .nav_hidden_text {
  animation-name: example;
  animation-duration: 1s;
  visibility: visible;
  width: 100%;
}

.cus_sub_nav {
  background: var(--cus-secondary) !important;
  font-size: 20px;

  li a {
    max-width: 320px;
    color: var(--cus-dark);
  }

  li:not(:last-child) a {
    margin-right: 100px;
  }
}

.nav_hidden_text {
  width: 0px;

  visibility: hidden;
}

.footer-logo-img {
  width: 200px;
  height: 200px;
  object-fit: contain;
}

@keyframes example {
  0% {
    width: 25px;
  }

  100% {
    width: 50px;
  }
}

@keyframes color {
  0% {
    background-color: rgba(255, 255, 255, 0);
    // box-shadow: 1px 3px 3px rgba(0, 0, 255, 0);
  }

  100% {
    background-color: rgb(255, 255, 255);
    // box-shadow: 1px 3px 3px blue;
  }
}

// bootstrap fix
@media (min-width: 1200px) {
  .container {
    max-width: 1300px;
  }
}
</style>
