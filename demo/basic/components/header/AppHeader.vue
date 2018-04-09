<template lang="html">
    <div id="header" class="clear">
        <h1>
            <a href="/" id="logo">
                <span>Logo</span>
            </a>
        </h1>
        <ul id="nav">
            <li>
                <form id="search-form">
                    <input type="text" id="search-query-nav" class="search-query">
                </form>
            </li>            
            <nav-dropdown-container v-for="menu in menus" v-bind:menu="menu" v-bind:key="menu.id" ></nav-dropdown-container>
        </ul>
    </div>
</template>

<script>
import NavDropdownContainer from '@/components/header/NavDropdownContainer'

export default {
  components: {
      NavDropdownContainer
  },
  name: "AppHeader",
  data () {
//   data: function(){
      return {
        menus: [
            {
                id: 1,
                name: 'Menu1',
                selected: true,
                submenus: [
                        { subname: 'Menu1-Sub1' },
                        { subname: 'Menu1-Sub2' },
                        { subname: 'Menu1-Sub3' },
                        { subname: 'Menu1-Sub4' }
                    ]
                               
            },
            {
                id: 2,
                name: 'Menu2',
                submenus: [
                        { subname: 'Menu2-Sub1' },
                        { subname: 'Menu2-Sub2' },
                        { subname: 'Menu2-Sub3' },
                        { subname: 'Menu2-Sub4' }
                ]
            },
            {
                id: 3,
                name: 'Menu3',
                submenus: [
                        { subname: 'Menu3-Sub1' },
                        { subname: 'Menu3-Sub2' },
                        { subname: 'Menu3-Sub3' },
                        { subname: 'Menu3-Sub4' }
                ]
            },
            {
                id: 4,
                name: 'Menu4',
                submenus: [
                        { subname: 'Menu3-Sub1' },
                        { subname: 'Menu3-Sub2' },
                        { subname: 'Menu3-Sub3' },
                        { subname: 'Menu3-Sub4' }
                ]
            }
        ]
      }
  }
}


</script>

<style scoped> 
#header {
  position: fixed;
  width: 100%;
  top: 0;
  background-color: #fff;
  height: 40px;
  padding: 10px 60px;
  z-index: 2;
}
body.docs #nav {
  position: fixed;
}
#nav {
  list-style-type: none;
  margin: 0;
  padding: 0;
  position: fixed;
  right: 30px;
  top: 10px;
  height: 40px;
  line-height: 40px;
}
#nav .break {
  display: none;
}
#nav li {
  display: inline-block;
  position: relative;
  margin: 0 0.6em;
}

#logo {
  display: inline-block;
  font-size: 1.5em;
  line-height: 40px;
  color: #2c3e50;
  font-family: "Dosis", "Source Sans Pro", "Helvetica Neue", Arial, sans-serif;
  font-weight: 500;
}
#logo img {
  vertical-align: middle;
  margin-right: 6px;
  width: 40px;
  height: 40px;
}
#header {
  box-shadow: 0 0 1px rgba(0,0,0,0.25);
  transition: background-color 0.3s ease-in-out;
}
@media screen and (max-width: 900px) {
   #header {
    display: none;
  }
  #logo {
    display: none;
  }    
}
 @media screen and (min-width: 1590px) {
  #header {
    background-color: rgba(255,255,255,0.4);
  }
}
</style>

