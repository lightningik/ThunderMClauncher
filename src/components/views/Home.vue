<template>
  <div class="hero">
    <div class="card-one">
      <div class="container">
        <h1>Thunder MC</h1>

        <a>Your personalized Minecraft Launcher</a>

        <div class="sidebar-items" :class="{active: isActive}">
          <router-link to="/">
            <button id="button-home">
              &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Home&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
            </button>
          </router-link>
          <div class="divider"/>
          <router-link to="/">
            <button id="button-mod">
              &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Mods&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
            </button>
          </router-link>
        </div>

        <button id="loginOptionMicrosoft" class="loginOptionButton">

          <i class="fa-brands fa-microsoft"></i>
          <span>Login with Microsoft</span>
        </button>


      </div>

    </div>
    <div class="card-two">
      <div class="container_two">

      </div>
    </div>
  </div>

</template>

<script>
import {FontAwesomeIcon} from "@fortawesome/vue-fontawesome";
import {computed} from "vue";
import {useRoute} from "vue-router";
export default {
  props: {
    to: { type: String, required: true },
  },
  name: "Home",
  components: {FontAwesomeIcon},
  setup(props){
    const route = useRoute()
    const isActive = computed(() => route.path === props.to)
    return { isActive }
  }
}


/**
const loginOptionMicrosoft = document.getElementById("loginOptionMicrosoft")

loginOptionMicrosoft.onclick = (e) => {

}
 **/
</script>

<style scoped>
@font-face {
  font-family: Montserrat;
  src: url('../../assets/fonts/Montserrat-VariableFont_wght.ttf')
}
.loginOptionButton {
  text-align: center;
  display: flex;
  justify-content: center;
}

.sidebar-items {

  display: inline-grid;
  align-content: center;
  align-items: center;
  justify-items: center;
}

.loginOptionButton i {
  width: 22px;
  height: 22px;
}

.card-one {
  border-radius: 50px;
  color: #BE83D4;
  background: #311432;
  box-shadow: 0 4px 8px 0 rgba(0, 0, 0, 0.2);
  font-family: "Montserrat", sans-serif;
  float: left;
  position: fixed;
  z-index: 1;
  top: 10px;
  padding: 0.5em;
  height: 700px;
  width: auto;
}

h1 {
  color: white;
}

.card-one:hover {
  box-shadow: 0 8px 16px 0 rgba(0,0,0,0.2);
}
.card-two:hover {
   box-shadow: 0 8px 16px 0 rgba(0,0,0,0.2);
 }

.card-two {
  border-radius: 50px;
  color: #BE83D4;
  box-shadow: 0 4px 8px 0 rgba(0, 0, 0, 0.2);
  font-family: "Montserrat", sans-serif;
  float: top;
  position: fixed;
  z-index: 1;
  top: 10px;
  right: 10px;
  padding: 0.5em;
  width: auto;
  height: 700px;
  background: #311432 url("dist/assets/hero.png") no-repeat center;
  background-size: cover;
  min-width: 1010px
}

.divider{
  height: 5px;
  display:inline-grid;
}

.hero {
  height: calc(100% - 60px);
}

.container {
  padding: 2px 16px;
}
.sidebar-items {
  padding: 1em;
}
.navicon {
  size: 30px;
  text-align: center;
}
</style>