<template lang="html">
    <div class="sidebar">
        <div class="sidebar-inner">
            <h2>Menu1</h2>
            <ul class="menu-root">
                <li><h3>Menu1-Subejct</h3></li>
                <li><a data-scroll href="#Menu1-1" class="sidebar-link">Menu1-1</a></li>
                <li><a data-scroll href="#Menu1-2" class="sidebar-link">Menu1-2</a></li>
                <li><a data-scroll href="#Menu1-3" class="sidebar-link">Menu1-3</a></li>
                <li><a data-scroll href="#Menu1-4" class="sidebar-link">Menu1-4</a></li>
            </ul>
        </div>
    </div>
</template>

<script>
export default {
    name: "AppSidebar"
}
</script>

<style scoped>
.sidebar {
  position: fixed;
  z-index: 10;
  top: 61px;
  left: 0;
  bottom: 0;
  overflow-x: hidden;
  overflow-y: auto;
  -webkit-overflow-scrolling: touch;
  -ms-overflow-style: none;
}
.sidebar h2 {
  margin-top: 0.2em;
}
.sidebar ul {
  list-style-type: none;
  margin: 0;
  line-height: 1.5em;
  padding-left: 1em;
}
.sidebar li {
  margin-top: 0.5em;
}
.sidebar .sidebar-inner {
  width: 200px;
  padding: 40px 20px 60px 60px;
}
.sidebar .version-select {
  vertical-align: middle;
  margin-left: 5px;
}
.sidebar .menu-root {
  padding-left: 0;
}
.sidebar .menu-sub {
  font-size: 0.85em;
}
.sidebar .sidebar-link {
  color: #7f8c8d;
}
.sidebar .sidebar-link.current {
  font-weight: 600;
  color: #03a9f4;
}
.sidebar .sidebar-link.new:after {
  content: "NEW";
  display: inline-block;
  font-size: 10px;
  font-weight: 600;
  color: #fff;
  background-color: #03a9f4;
  line-height: 14px;
  padding: 0 4px;
  border-radius: 3px;
  margin-left: 5px;
  vertical-align: middle;
  position: relative;
  top: -1px;
}
.sidebar .sidebar-link:hover {
  border-bottom: 2px solid #03a9f4;
}
.sidebar .section-link.active {
  font-weight: bold;
  color: #03a9f4;
}
.sidebar .main-menu {
  margin-bottom: 20px;
  display: none;
  padding-left: 0;
}
.sidebar .main-sponsor {
  color: #7f8c8d;
  font-size: 0.85em;
}
.sidebar .main-sponsor .logo {
  color: #7f8c8d;
  margin-top: 6px;
  text-align: center;
  font-weight: bold;
  display: block;
}
.sidebar .main-sponsor .logo:first-child {
  margin-top: 12px;
}
.sidebar .main-sponsor .logo:last-child {
  margin-bottom: 12px;
}
.sidebar .main-sponsor img,
.sidebar .main-sponsor a {
  width: 125px;
}
.sidebar .become-backer {
  border: 1px solid #03a9f4;
  border-radius: 2em;
  display: inline-block;
  color: #03a9f4;
  font-size: 0.8em;
  width: 125px;
  padding: 4px 0;
  text-align: center;
  margin-bottom: 20px;
}
.sidebar .nav-dropdown h4 {
  font-weight: normal;
  margin: 0;
}
@media screen and (max-width: 900px) {
  .sidebar {
    position: fixed;
    z-index: 10;
    background-color: #f9f9f9;
    height: 100%;
    top: 0;
    left: 0;
    box-shadow: 0 0 10px rgba(0,0,0,0.2);
    transition: all 0.4s cubic-bezier(0.4, 0, 0, 1);
    -webkit-transform: translate(-280px, 0);
    transform: translate(-280px, 0);
  }
  .sidebar .sidebar-inner {
    padding: 50px 10px 10px 20px;
    box-sizing: border-box;
  }
  .sidebar .sidebar-inner-index {
    padding: 10px 10px 10px 20px;
  }
  .sidebar .search-query {
    width: 200px;
    margin-bottom: 10px;
  }
  .sidebar .main-menu {
    display: block;
  }
  .sidebar.open {
    -webkit-transform: translate(0, 0);
    transform: translate(0, 0);
  }
}

</style>


