<template lang="html">
  <li class="nav-dropdown-container">
    <a class="nav-link" v-bind:class="{ current: menu.selected }">{{menu.name}}</a>
    <span class="arrow"></span>
    <ul class="nav-dropdown">
       <li>
          <ul>
              <li v-for="submenu in menu.submenus" ><a href="#" class="nav-link">{{submenu.subname}}</a></li>
          </ul>
      </li>
    </ul>
  </li>
</template>

<script>

export default {

  name: "NavDropdownContainer",
  props: ['menu']   
}
</script>

<style scoped>

#nav .nav-link {
  cursor: pointer;
}
.nav-dropdown-container>.nav-link:hover,
.nav-link.current {
    border-bottom: 2px solid #03a9f4;
  }

#nav .nav-dropdown-container:hover .nav-dropdown {
  display: block;
}
#nav .nav-dropdown-container.language,
#nav .nav-dropdown-container.ecosystem {
  margin-left: 20px;
}
#nav .nav-dropdown-container .arrow {
  pointer-events: none;
}
#nav .nav-dropdown {
  display: none;
  box-sizing: border-box;
  max-height: calc(100vh - 61px);
  overflow-y: auto;
  position: absolute;
  top: 100%;
  right: -15px;
  background-color: #fff;
  padding: 10px 0;
  border: 1px solid #ddd;
  border-bottom-color: #ccc;
  text-align: left;
  border-radius: 4px;
  white-space: nowrap;
}
#nav .nav-dropdown li {
  line-height: 1.8em;
  margin: 0;
  display: block;
}
#nav .nav-dropdown li > ul {
  padding-left: 0;
}
#nav .nav-dropdown li:first-child h4 {
  margin-top: 0;
  padding-top: 0;
  border-top: 0;
}
#nav .nav-dropdown a,
#nav .nav-dropdown h4 {
  padding: 0 24px 0 20px;
}
#nav .nav-dropdown h4 {
  margin: 0.45em 0 0;
  padding-top: 0.45em;
  border-top: 1px solid #eee;
}
#nav .nav-dropdown a {
  color: #3a5169;
  font-size: 0.9em;
  display: block;
}
#nav .nav-dropdown a:hover {
  color: #03a9f4;
}
#nav .arrow {
  display: inline-block;
  vertical-align: middle;
  margin-top: -1px;
  margin-left: 2px;
  margin-right: -14px;
  width: 0;
  height: 0;
  border-left: 4px solid transparent;
  border-right: 4px solid transparent;
  border-top: 5px solid #ccc;
}
.new-label {
  position: absolute;
  top: 3px;
  left: 110%;
  background-color: #03a9f4;
  color: #fff;
  line-height: 16px;
  height: 16px;
  font-size: 9px;
  font-weight: bold;
  font-family: "Roboto Mono", Monaco, courier, monospace;
  padding: 1px 4px 0 6px;
  border-radius: 4px;
}
  
</style>


