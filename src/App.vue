<template>
	<div id="app">
		<!-- <img src="./assets/logo.png"> -->
		<!-- <app-ficheiro></app-ficheiro> -->
		<!-- <router-view/> -->

		<el-container style="height: 100%; border: 0px solid #eee">
			<el-aside width="200px">
				<el-menu :default-openeds="['', '']">
					<el-submenu index="1">
						<template slot="title">
							<i class="el-icon-message"></i>Navigator One</template>
						<el-menu-item-group title="Group 2">
							<el-menu-item index="1-3">Option 3</el-menu-item>
						</el-menu-item-group>
						<el-submenu index="1-4">
							<template slot="title">Option4</template>
							<el-menu-item index="1-4-1">Option 4-1</el-menu-item>
						</el-submenu>
					</el-submenu>
					<el-submenu index="2">
						<template slot="title">
							<i class="el-icon-menu"></i>Navigator Two</template>
						<el-menu-item-group>
							<template slot="title">Group 1</template>
							<el-menu-item index="2-1">Option 1</el-menu-item>
							<el-menu-item index="2-2">Option 2</el-menu-item>
						</el-menu-item-group>
						<el-menu-item-group title="Group 2">
							<el-menu-item index="2-3">Option 3</el-menu-item>
						</el-menu-item-group>
						<el-submenu index="2-4">
							<template slot="title">Option 4</template>
							<el-menu-item index="2-4-1">Option 4-1</el-menu-item>
						</el-submenu>
					</el-submenu>
					<el-submenu index="3">
						<template slot="title">
							<i class="el-icon-setting"></i>Navigator Three</template>
						<el-menu-item-group>
							<template slot="title">Group 1</template>
							<el-menu-item index="3-1">Option 1</el-menu-item>
							<el-menu-item index="3-2">Option 2</el-menu-item>
						</el-menu-item-group>
						<el-menu-item-group title="Group 2">
							<el-menu-item index="3-3">Option 3</el-menu-item>
						</el-menu-item-group>
						<el-submenu index="3-4">
							<template slot="title">Option 4</template>
							<el-menu-item index="3-4-1">Option 4-1</el-menu-item>
						</el-submenu>
					</el-submenu>
				</el-menu>
			</el-aside>

			<el-container>
				<el-header style="text-align: right; font-size: 12px">
					<el-dropdown>
						<i class="el-icon-setting" style="margin-right: 15px"></i>
						<el-dropdown-menu slot="dropdown">
							<el-dropdown-item>View</el-dropdown-item>
							<el-dropdown-item>Add</el-dropdown-item>
							<el-dropdown-item>Delete</el-dropdown-item>
						</el-dropdown-menu>
					</el-dropdown>
					<span>Tom</span>
				</el-header>

				<el-main>
					<h4>Main content</h4>
				</el-main>
			</el-container>
		</el-container>

	</div>
</template>

<script>
// import Ficheiro from "./Ficheiro.vue";
// export default {
// components: {
//   // "app-ficheiro": Ficheiro
// }

import element from "element-ui";
import "element-ui/lib/theme-chalk/index.css";

export default {
  components: {
    // "app-ficheiro": Ficheiro
    "elem-button": element.Button,
    "elem-slider": element.Slider,
    "elem-collapse": element.Collapse,
    "elem-collapse-item": element.CollapseItem,
    "el-container": element.Container,
    "el-aside": element.Aside,
    "el-header": element.Header,
    "el-table-column": element.TableColumn,
    "el-main": element.Main,
    "el-dropdown": element.Dropdown,
    "el-dropdown-menu": element.DropdownMenu,
    "el-dropdown-item": element.DropdownItem,
    "el-menu": element.Menu,
    "el-submenu": element.Submenu,
    "el-menu-item-group": element.MenuItemGroup,
    "el-menu-item": element.MenuItem
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

h1,
h2 {
  font-weight: normal;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
.el-header {
  background-color: #b3c0d1;
  color: #333;
  line-height: 60px;
}

.el-aside {
  color: #333;
}
</style>