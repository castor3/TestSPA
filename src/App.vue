<template>
	<div id="app">
		<!-- <img src="./assets/logo.png"> -->
		<!-- <router-view/> -->
		<!--
			## Dark theme ##
			background-color="#545c64"
			text-color="#fff"
			active-text-color="#ffd04b"
		-->
		<el-container>
			
			<!-- collapsed = value sent to 'app-navbar' -->
			<app-navbar :collapsed = isCollapsed />

			<!-- collapseChanged = event thrown by 'app-main' -->
			<!-- '$event' = value sent by the event -->
			<app-main @collapseChanged="isCollapsed = $event" />
		
		</el-container>
	</div>
</template>


<script>
import element from "element-ui";
import "element-ui/lib/theme-chalk/index.css";

import NavBar from "./components/shared/NavBar.vue";
import Main from "./components/Main.vue";

export default {
  components: {
    "app-navbar": NavBar,
    "app-main": Main,
    // NavBar
    "el-menu": element.Menu,
    "el-submenu": element.Submenu,
    "el-menu-item-group": element.MenuItemGroup,
    "el-menu-item": element.MenuItem,

    "el-container": element.Container
  },
  data() {
    return {
      isCollapsed: true	// property to receive value from 'main', and send to 'navbar'
    };
  }
};
</script>


<style>
body {
  margin: 0; /* To give the 'SPA' look */
}
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
.el-menu-vertical-demo:not(.el-menu--collapse) {
  width: 200px;
  /* min-height: 400px; */
  height: 100%;
  border-width: 0px;
}
</style>