<script>
export default {
  name: "NavBarHeader",
  props: {
    listMenu: Array
  },
  data() {
    return {
      currentMenuItem: null,          //voci del menu nell header
      showMenu: false,
      activeItem: null

    }
  },
  methods: {
    setMenuItem(item) {                 //voci del menu nell header
      this.currentMenuItem = item;
    },
    toggleHamburger() {           
      this.showMenu = !this.showMenu;
    },
    setActiveItem(index) {
      this.activeItem = index;
      this.showMenu = false;
    },
    closeHamburger() {
      this.showMenu = false;
    }
  }
}

</script>

<!-- ►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►► -->

<template>
  
  <section class="navbarheader">

    <!-- HAMBURGER MENU -->

    <nav>
      <div id="hamburger" @click="toggleHamburger">
        <i class="fa-solid fa-bars"></i>
        <ul id="hamburger-menu" :class="{ show: showMenu }">
          <li id="ics" @click="closeHamburger">
            <i class="fa-solid fa-xmark"></i>
          </li>
          <li class="p-1" v-for="(listitem, index) in listMenu" :key="index" :class="{ active: activeItem === index }">
            <a href="#" @click="setActiveItem(index)">{{ listitem }}</a>
          </li>
        </ul>
      </div>
    </nav>


    <!-- MENU STANDARD -->
    
    <ul class="d-none d-md-flex flex-md-row gap-3 m-0 align-items-center">
      <li v-for="(listitem, index) in listMenu" :key="index" :class="{ active: currentMenuItem === listitem }"
        @click="setMenuItem(listitem)">
        <a href="#">{{ listitem }}</a>
      </li>
      <li>
        <a href=""><img src="../assets/svg/svg-1.svg" alt=""></a>
      </li>
    </ul>
  </section>
</template>
    
<!-- In questo modo, quando viene cliccato un elemento del menu, VueJS aggiungerà la classe active a quell'elemento
  , attivando la regola CSS &.active:after, che applicherà la sottolineatura verde all'elemento cliccato.
  Allo stesso tempo, VueJS rimuoverà la classe active dall'elemento precedente, rimuovendo la sottolineatura verde -->

<!-- ►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►►► -->

<style lang="scss" scoped>
@use "../style/general.scss" as *;
@use "../style/partials/variables.scss" as *;

#hamburger {
  display: none;
}

@media (max-width: 768px) {
  #hamburger {
    display: block;
    cursor: pointer;

    i {
      font-size: 1.5rem;
    }

    #hamburger-menu {
      display: none;
      position: absolute;
      top: 100%;
      right: 0;
      color: $btn-border;
      background-color: #211f38eb;
      padding: 1rem;
      width: 100%;
      z-index: 998;

      &.show {
        display: block;
        width: 200px;
        font-size: .9rem;
      }
o     
      & li a {
        display: block;
        color: green;
        padding: 0.5rem 0;
        font-weight: bold;
        transition: all 0.3s ease;
      }

      #ics {
        position: absolute;
        right: 7px;
        top: 5px;
      }
    }

    & li.active a {
      color: $btn-border;

    }

  }
}


ul {
  li {

    font-weight: 600;
    position: relative;
    font-size: .8rem;

    &:after {
      content: '';
      position: absolute;
      bottom: -5px;
      left: 0;
      width: 100%;
      height: 2px;
      background-color: $btn-border;
      transform: scaleX(0);
      transition: transform 0.3s ease-out;
      transform-origin: center;
    }

    &.active:after {
      transform: scaleX(1);
    }
  }

  img {
    width: 15px;
    height: 15px;
    vertical-align: text-bottom;
    margin-right: 10px;
  }

}
</style>
