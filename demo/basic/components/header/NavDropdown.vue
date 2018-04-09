<template lang="html">
    <li>
        <h4>{{menu.subtitle}}</h4>
        <ul>
            <li><a href="#" class="nav-link">{{menu.subname}}</a></li>
        </ul>
    </li>
</template>

<script>

export default {
    name: "NavDropdown",
    propt: ["menu"] 
}
</script>

<style scoped>
#nav .nav-link {
  cursor: pointer;
}
#nav .nav-dropdown-container .nav-link:hover:not(.current) {
  border-bottom: none;
}
#nav .nav-dropdown .nav-link:hover,
#nav .nav-dropdown .nav-link.current {
  border-bottom: none;
}
.nav-link:hover,
.nav-link.current {
  border-bottom: 3px solid #03a9f4;
}
#nav .nav-dropdown .nav-link.current::after {
  content: "";
  width: 0;
  height: 0;
  border-left: 5px solid #03a9f4;
  border-top: 3px solid transparent;
  border-bottom: 3px solid transparent;
  position: absolute;
  top: 50%;
  margin-top: -4px;
  left: 8px;
}
.nav-link {
  display:inline-block;
  padding-bottom: 3px;
  white-space: nowrap;
}
.nav-link.team {
  margin-left: 10px;
}
@media screen and (max-width: 900px) {
  .nav-link {
    padding-bottom: 1px;
  }
  .nav-link:hover,
  .nav-link.current {
    border-bottom: 2px solid #03a9f4;
  }   
}
</style>


