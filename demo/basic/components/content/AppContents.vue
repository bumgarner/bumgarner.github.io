<template lanh="html">
    <div class="content">
        <h2>Menu1</h2>
        <h3 id="Menu1-1" data-scroll-id="Menu1-1">Menu1-1</h3>
        <p>content text content text content text content text content text content text content text content text content text content text content text content text content text content text content text content text content text content text content text content text content text content text content text content text content text content text content text content text content text content text content text content text content text content text content text content text content text content text content text content text content text content text content text content text content text content text content text content text content text content text content text content text content text content text content text content text content text content text content text content text content text content text</p>
        <h3 id="Menu1-2" data-scroll-id="Menu1-2">Menu1-2</h3>
        <p>content text content text content text content text content text content text content text content text content text content text content text content text content text content text content text content text content text content text content text content text content text content text content text content text content text content text content text content text content text content text content text content text content text content text content text content text content text content text content text content text content text content text content text content text content text content text content text content text content text content text content text content text content text content text content text content text content text content text content text content text content text content text</p>
        <h3 id="Menu1-3" data-scroll-id="Menu1-3">Menu1-3</h3>
        <p>content text content text content text content text content text content text content text content text content text content text content text content text content text content text content text content text content text content text content text content text content text content text content text content text content text content text content text content text content text content text content text content text content text content text content text content text content text content text content text content text content text content text content text content text content text content text content text content text content text content text content text content text content text content text content text content text content text content text content text content text content text content text</p>
        <h3 id="Menu1-4" data-scroll-id="Menu1-4">
            <a data-scroll>Menu1-4</a>
        </h3>
        <p>content text content text content text content text content text content text content text content text content text content text content text content text content text content text content text content text content text content text content text content text content text content text content text content text content text content text content text content text content text content text content text content text content text content text content text content text content text content text content text content text content text content text content text content text content text content text content text content text content text content text content text content text content text content text content text content text content text content text content text content text content text content text</p>
    </div>
</template>

<script>
export default {
  name: "AppContents"
}
</script>

<style scoped>
.content.menu {
  font-size: 1.2em;
}
.content.menu .menu-root {
  padding-left: 0;
}
.content.menu #search-form,
.content.menu .algolia-autocomplete,
.content.menu input {
  width: 100%;
}
.content.menu .aa-dropdown-menu {
  box-sizing: border-box;
}
.content.menu h3 {
  margin: 1.5em 0 0.75em;
}
.content.menu h3:before,
.content.menu h3:after {
  display: none;
}
.content.menu li {
  list-style-type: none;
  margin-top: 0.1em;
}
.content {
  position: relative;
  padding: 2.2em 0;
  max-width: 600px;
  margin: 0 auto;
  padding-left: 150px;
}
.content a.button {
  font-size: 0.9em;
  color: #fff;
  margin: 0.2em 0;
  width: 180px;
  text-align: center;
  padding: 12px 24px;
  display: inline-block;
  vertical-align: middle;
}
.content img {
  max-width: 100%;
}
.content h1 {
  margin: 0 0 1em;
}
.content h2,
.content h3 {
  pointer-events: none;
}
.content h2 a,
.content h3 a {
  pointer-events: auto;
  color: #2c3e50;
}
.content h2:before,
.content h3:before {
  content: "";
  display: block;
  margin-top: -91px;
  height: 91px;
  visibility: hidden;
}
.content h2 {
  margin: 45px 0 0.8em;
  padding-bottom: 0.7em;
  border-bottom: 1px solid #ddd;
}
.content h3 {
  margin: 52px 0 1.2em;
  position: relative;
}
.content h3:after {
  content: "#";
  color: #03a9f4;
  position: absolute;
  left: -0.7em;
  bottom: -2px;
  font-size: 1.2em;
  font-weight: bold;
}
.content p,
.content ul,
.content ol {
  line-height: 1.6em;
  margin: 1.2em 0 -1.2em;
  padding-bottom: 1.2em;
  position: relative;
  z-index: 1;
}
.content ul,
.content ol {
  padding-left: 1.5em;
  position: inherit;
}
.content a {
  color: #03a9f4;
  font-weight: 600;
}
@media screen and (max-width: 900px) {
  .content {
    padding-left: 0;
  }
  .content.with-sidebar {
    margin: auto;
  }
  .content h2:before,
  .content h3:before {
    content: "";
    display: block;
    margin-top: -70px;
    height: 70px;
    visibility: hidden;
  }
}
@media screen and (max-width: 1300px) {
  .content.with-sidebar {
    margin-left: 290px;
  }    
}
</style>


