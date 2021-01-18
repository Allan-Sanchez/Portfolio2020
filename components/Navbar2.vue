<template>
  <div >
    <div class="main-menu">
      <b-navbar
        class="navbar navbar-light color-nav p-lg-0 fixed-nav"
        toggleable="lg"
      >
        <b-navbar-brand class="nav-item-logo-port" href="#">
          Allan Sanchez
        </b-navbar-brand>
        <b-navbar-toggle target="nav-collapse"></b-navbar-toggle>

        <b-collapse id="nav-collapse" is-nav>
          <div class="mr-auto"></div>
          <b-navbar-nav id="patherNav" class="pather-nav">
            <b-nav-item
              class="nav-item-portfolio efect-nav nav-actived"
              to="/"
              >{{ $t("Navbar.home") }}</b-nav-item
            >
            <b-nav-item
              class="nav-item-portfolio efect-nav"
              href="#section-about"
              >{{ $t("Navbar.about") }}</b-nav-item
            >
            <b-nav-item
              class="nav-item-portfolio efect-nav"
              href="#section-skill"
              >{{ $t("Navbar.skil") }}</b-nav-item
            >
            <b-nav-item
              class="nav-item-portfolio efect-nav"
              href="#section-contact"
              >{{ $t("Navbar.contact") }}</b-nav-item
            >
          </b-navbar-nav>

          <b-navbar-nav class="ml-auto">
            <b-nav-item-dropdown
              class="nav-item-portfolio efect-nav"
              :text="$t('Navbar.language')"
              right
            >
              <!-- <nuxt-link: to = "switchLocalePath ('en')" class="nav-item-portfolio" > italiano </nuxt-link>  -->
              <b-dropdown-item
                class="nav-item-portfolio"
                :to="switchLocalePath('en')"
                >EN</b-dropdown-item
              >
              <b-dropdown-item
                class="nav-item-portfolio"
                :to="switchLocalePath('es')"
                >ES</b-dropdown-item
              >
            </b-nav-item-dropdown>

            <b-nav-item>
              <button
                :class="themeActive"
                @click="toggleTheme()"
                class="switch-theme mt-2"
                id="switch-theme"
              >
                <span class="">
                  <svg
                    style="vertical-align: sub"
                    width="20"
                    height="20"
                    viewBox="0 0 48 48"
                  >
                    <title>ic_wb_sunny_48px</title>
                    <g fill="#eff312">
                      <path
                        d="M13.51 9.69L9.93 6.1 7.1 8.93l3.59 3.59 2.82-2.83zM8 21H2v4h6v-4zM26 1.1h-4V7h4V1.1zm14.9 7.83L38.07 6.1l-3.59 3.59 2.83 2.83 3.59-3.59zm-6.41 27.38l3.59 3.59 2.83-2.83-3.59-3.59-2.83 2.83zM40 21v4h6v-4h-6zM24 11c-6.63 0-12 5.37-12 12s5.37 12 12 12 12-5.37 12-12-5.37-12-12-12zm-2 33.9h4V39h-4v5.9zM7.1 37.07l2.83 2.83 3.59-3.59-2.83-2.83-3.59 3.59z"
                      ></path>
                    </g>
                  </svg>
                </span>
                <span>
                  <svg
                    style="vertical-align: sub"
                    width="20"
                    height="20"
                    viewBox="0 0 512 512"
                  >
                    <title>moon</title>
                    <g fill="#fff">
                      <path
                        d="M283.211 512c78.962 0 151.079-35.925 198.857-94.792 7.068-8.708-.639-21.43-11.562-19.35-124.203 23.654-238.262-71.576-238.262-196.954 0-72.222 38.662-138.635 101.498-174.394 9.686-5.512 7.25-20.197-3.756-22.23A258.156 258.156 0 0 0 283.211 0c-141.309 0-256 114.511-256 256 0 141.309 114.511 256 256 256z"
                      ></path>
                    </g>
                  </svg>
                </span>
              </button>
            </b-nav-item>
          </b-navbar-nav>
        </b-collapse>
      </b-navbar>
      <div class="bar-nav">
        <div class="progress-bar-nav" id="myBar"></div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  // props:['mode'],
  data() {
    return {
      checked: false,
      themeActive: "",
    };
  },
  methods: {
    toggleMode() {
      this.checked = !this.checked;
    },
    toggleTheme() {
      if (this.themeActive === "active") {
        this.themeActive = "";
        this.$emit("Changemode");
      } else {
        this.themeActive = "active";
        this.$emit("Changemode");
      }
    },
    handleScroll() {
      // Your scroll handling here
      console.log(window.scrollY);
      var winScroll =
        document.body.scrollTop || document.documentElement.scrollTop;
      var height =
        document.documentElement.scrollHeight -
        document.documentElement.clientHeight;
      var scrolled = (winScroll / height) * 100;
      document.getElementById("myBar").style.width = scrolled + "%";
    },
  },
  beforeMount() {
    window.addEventListener("scroll", this.handleScroll);
  },
  beforeDestroy() {
    window.removeEventListener("scroll", this.handleScroll);
  },
};
</script>

<style>

.main-menu{
position: relative;
width: 100%;
height: 150px;
z-index: 1;
}
.fixed-nav{
    position: fixed;
    width: 100%;
}


.dropdown-menu {
  background: var(--background-navbar) !important;
}
.color-nav {
  /* padding: 0% !important; */
  box-shadow: 0px 4px 12px var(--shadow-navbar);
  background: var(--background-navbar);
}
.bar-nav {
  display: block;
  width: 100%;
  background: transparent;
  border-bottom: 6px solid var(--border-navbar);
  position: fixed;
  z-index: 1;
  top: 72px;
}
.progress-bar-nav {
  position: absolute;
  background: var(--gradient-color);
  height: 10px;
  width: 0%;
  margin-bottom: -6px;
  transition: width 0.3s ease-out;
}
.nav-item-logo-port {
  margin-left: 20px;
  font-family: "Roboto", sans-serif;
  text-transform: uppercase;
  position: relative;
  /* color: var(--title-color) !important; */
  font-weight: bold;
  padding: 5px 10px;
  background: var(--gradient-color);
  -webkit-text-fill-clip: text;
  -webkit-text-fill-color: transparent;
  background-clip: text;
}

.nav-item-portfolio {
  /* font: normal 500 15px/2px var(--roboto); */
  font-family: "Roboto", sans-serif;
  text-transform: uppercase;
  font-weight: bold;
  padding: 1rem;
  color: var(--title-color) !important;
  /* color:  red !important; */
}
.nav-item-portfolio a {
  color: var(--title-color) !important;
}
.nav-item-portfolio.nav-actived {
  background: var(--gradient-color);
  -webkit-text-fill-clip: text;
  -webkit-text-fill-color: transparent;
  background-clip: text;
}

.nav-item-portfolio :hover {
  background: var(--gradient-color);
  -webkit-text-fill-clip: text;
  -webkit-text-fill-color: transparent;
  background-clip: text;
}

.nav-item-logo-port:before {
  content: "";
  position: absolute;
  bottom: 0px;
  left: 0px;
  width: 12px;
  height: 12px;
  border: 3px solid var(--primary-color);
  border-width: 0 0 3px 3px;
  transition: 0.5s;
  /* opacity: 1; */
}

.nav-item-logo-port:after {
  content: "";
  position: absolute;
  top: 0px;
  right: 0px;
  width: 12px;
  height: 12px;
  border: 3px solid var(--primary-color);
  border-width: 3px 3px 0 0;
  transition: 0.5s;
  /* opacity: 1; */
}

.pather-nav li {
  position: relative;
  /* padding: 5px 10px; */
}

.efect-nav:before {
  content: "";
  position: absolute;
  bottom: 25px;
  left: 25px;
  width: 12px;
  height: 12px;
  border: 3px solid var(--primary-color);
  border-width: 0 0 3px 3px;
  transition: 0.5s;
  opacity: 0;
}
.efect-nav:hover.efect-nav::before {
  bottom: 15px;
  left: 15px;
  opacity: 1;
}

.efect-nav:hover.efect-nav:after {
  top: 15px;
  right: 15px;
  opacity: 1;
}

.efect-nav:after {
  content: "";
  position: absolute;
  top: 25px;
  right: 25px;
  width: 12px;
  height: 12px;
  border: 3px solid var(--primary-color);
  border-width: 3px 3px 0 0;
  transition: 0.5s;
  opacity: 0;
}

/* toggle theme  switch*/
.switch-theme {
  background: #343d5b;
  border-radius: 1000px;
  border: none;
  position: relative;
  display: flex;
  cursor: pointer;
  outline: none;
}
.switch-theme::after {
  content: "";
  display: block;
  width: 32px;
  height: 32px;
  position: absolute;
  background: #f1f1f1;
  top: 0;
  left: 0;
  right: unset;
  border-radius: 100px;
  transition: 0.3s ease all;
  box-shadow: 0px 0px 2px 2px rgba(0, 0, 0, 0.2);
}

.switch-theme.active {
  background: #f3f7f9;
  color: #000;
}
.switch-theme.active::after {
  right: 0;
  left: unset;
}

.switch-theme span {
  width: 30px;
  height: 30px;
  line-height: 30px;
  /* display: block; */
  background: none;
  color: #fff;
}

@media (max-width: 992px) { 
.bar-nav{
    top: 50px;
}    
 }
@media only screen and (max-width: 990px) {
  .efect-nav:hover.efect-nav:after {
    opacity: 0;
  }

  .efect-nav:hover.efect-nav:before {
    opacity: 0;
  }
}
</style>
