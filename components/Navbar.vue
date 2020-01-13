<template>
    <div>
        <header class="header_area">
            <div class="main-menu">
                <b-navbar class="navbar navbar-light" toggleable="lg">
                    <b-navbar-brand class="nav-item-logo-port" href="#">
                            Allan Sanchez
                    </b-navbar-brand>
                  <b-navbar-toggle target="nav-collapse"></b-navbar-toggle>

                  <b-collapse id="nav-collapse" is-nav>
                  <div class="mr-auto"></div>
                    <b-navbar-nav id="patherNav" class="pather-nav">
                      <b-nav-item class="nav-item-portfolio efect-nav nav-actived" href="#">{{ $t('Navbar.home') }}</b-nav-item>
                      <b-nav-item class="nav-item-portfolio efect-nav" href="#">{{ $t('Navbar.about') }}</b-nav-item>
                      <b-nav-item class="nav-item-portfolio efect-nav" href="#">{{ $t('Navbar.skil') }}</b-nav-item>
                      <b-nav-item class="nav-item-portfolio efect-nav" href="#">{{ $t('Navbar.contact') }}</b-nav-item>
                    </b-navbar-nav>

                    <b-navbar-nav class="ml-auto">
                        <b-nav-item-dropdown class="nav-item-portfolio efect-nav" :text="$t('Navbar.language')" right>
                          <b-dropdown-item class="nav-item-portfolio" href="#">EN</b-dropdown-item>
                          <b-dropdown-item class="nav-item-portfolio" href="#">ES</b-dropdown-item>
                        </b-nav-item-dropdown>

                        <b-nav-item href="#" class="nav-item-portfolio" @click="toggleMode()" >
                            <b-form-checkbox  v-model="checked"  size="md"  switch>
                              <span class="" v-if="checked">{{ $t('Navbar.dark') }}</span>
                              <span class="" v-else>{{ $t('Navbar.light') }}</span>
                            </b-form-checkbox>
                        </b-nav-item>
                    </b-navbar-nav>
                  </b-collapse>

                </b-navbar>
            </div>
        </header>
        
    </div>
</template>

<script>
export default {
    data() {
        return {
            checked: false,
        }
    },
    methods: {
        toggleMode(){
            this.checked = !this.checked;
        }
    },
}
</script>

<style >
.nav-item-logo-port{
    margin-left: 20px;
    font-family: 'Roboto',sans-serif;
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

.nav-item-portfolio{
    /* font: normal 500 15px/2px var(--roboto); */
    font-family: 'Roboto', sans-serif;
    text-transform: uppercase;
    font-weight: bold;  
    padding: 1rem;
    color: var(--title-color) !important;
    /* color:  red !important; */
}
.nav-item-portfolio a{
    color: var(--title-color) !important;
}
.nav-item-portfolio.nav-actived{
    background: var(--gradient-color);
    -webkit-text-fill-clip: text;
    -webkit-text-fill-color: transparent;
    background-clip: text; 
}

.nav-item-portfolio :hover{
     background: var(--gradient-color);
    -webkit-text-fill-clip: text;
    -webkit-text-fill-color: transparent;
    background-clip: text; 
}

.nav-item-logo-port:before{
    content: '';
    position: absolute;
    bottom: 0px;
    left: 0px;
    width: 12px;
    height: 12px;
    border: 3px solid var(--primary-color);
    border-width: 0 0 3px 3px;
    transition: .5s;
    /* opacity: 1; */
}

.nav-item-logo-port:after{
    content: '';
    position: absolute;
    top: 0px;
    right: 0px;
    width: 12px;
    height: 12px;
    border: 3px solid var(--primary-color);
    border-width: 3px 3px 0 0;
    transition: .5s;
    /* opacity: 1; */
}

.pather-nav li {
        position: relative;
         /* padding: 5px 10px; */
}


.efect-nav:before{
    content: '';
    position: absolute;
    bottom: 25px;
    left: 25px;
    width: 12px;
    height: 12px;
    border: 3px solid var(--primary-color);
    border-width: 0 0 3px 3px;
    transition: .5s;
    opacity: 0;
}
.efect-nav:hover.efect-nav::before{
    bottom: 15px;
    left:15px;
    opacity: 1;
}

.efect-nav:hover.efect-nav:after{
    top: 15px;
    right:15px;
    opacity: 1;
}

.efect-nav:after{
    content: '';
    position: absolute;
    top: 25px;
    right: 25px;
    width: 12px;
    height: 12px;
    border: 3px solid var(--primary-color);
    border-width: 3px 3px 0 0;
    transition: .5s;
    opacity: 0;
}

@media only screen and (max-width: 990px){
    .efect-nav:hover.efect-nav:after{
        opacity: 0;
    }

     .efect-nav:hover.efect-nav:before{
        opacity: 0;
    }
}

</style>