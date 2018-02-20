<template>
	<div id="app">
		<!-- <img src="./assets/logo.png"> -->
		<!-- <app-ficheiro></app-ficheiro> -->
		<!-- <router-view/> -->

		<el-container>
			<el-menu style="height:100%" class="el-menu-vertical-demo"
							@open="handleOpen" @close="handleClose" :collapse="isCollapsed">
				<!-- Main window -->
				<el-submenu index="1">
					<template slot="title">
						<i class="el-icon-message"></i>
						<span slot="title">Main window</span>
					</template>
					<el-menu-item-group title="Group 2">
						<el-menu-item index="1-1">Option 1</el-menu-item>
					</el-menu-item-group>
					<el-submenu index="1-2">
						<template slot="title">Option2</template>
						<el-menu-item index="1-4-1">Option 2-1</el-menu-item>
					</el-submenu>
				</el-submenu>
				<!-- Friends -->
				<el-submenu index="2">
					<template slot="title">
						<i class="el-icon-menu"></i>
						<span slot="title">Friends</span>
					</template>
					<el-menu-item-group>
						<template slot="title">Group 1</template>
						<el-menu-item index="2-1">Option 1</el-menu-item>
					</el-menu-item-group>
					<el-menu-item-group title="Group 2">
						<el-menu-item index="2-3">Option 2</el-menu-item>
					</el-menu-item-group>
					<el-submenu index="2-4">
						<template slot="title">Option 4</template>
						<el-menu-item index="2-4-1">Option 4-1</el-menu-item>
					</el-submenu>
				</el-submenu>
				<!-- Fields -->
				<el-submenu index="3">
					<template slot="title">
						<i class="el-icon-location"></i>
						<span slot="title">Fields</span>
					</template>
					<el-menu-item-group>
						<template slot="title">Group 1</template>
						<el-menu-item index="3-1">Option 1</el-menu-item>
						<el-menu-item index="3-2">Option 2</el-menu-item>
					</el-menu-item-group>
					<el-submenu index="3-4">
						<template slot="title">Option 4</template>
						<el-menu-item index="3-4-1">Option 4-1</el-menu-item>
					</el-submenu>
				</el-submenu>
				<!-- Profile -->
				<el-submenu index="4">
					<template slot="title">
						<i class="el-icon-setting"></i>
						<span slot="title">Profile</span>
					</template>
				</el-submenu>
				<!-- Settings -->
				<el-submenu index="5">
					<template slot="title">
						<i class="el-icon-setting"></i>
						<span slot="title">Settings</span>
					</template>
				</el-submenu>
			</el-menu>

			<el-container>
				<app-main @collapseChanged="isCollapsed = $event">
					<!-- Header and Main -->
				</app-main>
			</el-container>
		</el-container>

	</div>
</template>

<script>
import element from "element-ui";
import "element-ui/lib/theme-chalk/index.css";

import NavBar from "./components/NavBar.vue";
import Main from "./components/Main.vue";

export default {
  components: {
    // "app-navbar": NavBar,
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
      isCollapsed: true
    };
  },
  methods: {
    handleOpen(key, keyPath) {
      console.log(key, keyPath);
    },
    handleClose(key, keyPath) {
      console.log(key, keyPath);
    }
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
li {
  display: inline-block;
  margin: 0 10px;
}
.el-menu-vertical-demo:not(.el-menu--collapse) {
  width: 200px;
  min-height: 400px;
}
.el-menu-item {
  text-align: left;
}
</style>