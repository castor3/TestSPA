<template>
	<div id="app">
		<!-- <img src="./assets/logo.png"> -->
		<!-- <app-ficheiro></app-ficheiro> -->
		<!-- <router-view/> -->

		<el-container>
			<el-menu default-active="2" class="el-menu-vertical-demo" default-openeds="['','']" @open="handleOpen" @close="handleClose" :collapse="isCollapse">
				<!-- Main window -->
				<el-submenu index="1">
					<template slot="title">
						<i class="el-icon-message"></i>
						<span slot="title">Main window</span>
					</template>
					<el-menu-item-group title="Group 2">
						<el-menu-item index="1-3">Option 3</el-menu-item>
					</el-menu-item-group>
					<el-submenu index="1-4">
						<template slot="title">Option4</template>
						<el-menu-item index="1-4-1">Option 4-1</el-menu-item>
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
				<el-header style="font-size: 12px">
					<el-row>
						<span style="float: left">
							<el-col>
								<!-- Collapse / Expand buttons -->
								<el-radio-group v-model="isCollapse">
									<el-radio-button :label="false">expand</el-radio-button>
									<el-radio-button :label="true">collapse</el-radio-button>
								</el-radio-group>
							</el-col>
						</span>
						<span style="float: right">
							<el-col>
								<!-- Right side options -->
								<el-dropdown>
									<i class="el-icon-setting" style="margin-right: 15px"></i>
									<el-dropdown-menu slot="dropdown">
										<el-dropdown-item>View</el-dropdown-item>
										<el-dropdown-item>Add</el-dropdown-item>
										<el-dropdown-item>Delete</el-dropdown-item>
									</el-dropdown-menu>
								</el-dropdown>
								<span>Tom</span>
							</el-col>
						</span>
					</el-row>
				</el-header>

				<!-- Main content -->
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

import element, { RadioButton } from "element-ui";
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
    "el-menu-item": element.MenuItem,
    "el-radio-group": element.RadioGroup,
    "el-radio-button": element.RadioButton,
    "el-row": element.Row,
    "el-col": element.Col,
    "el-table": element.ta
  },
  data() {
    return {
      isCollapse: true
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
  text-align: center;
  line-height: 60px;
}
.el-main {
  background-color: #e9eef3;
  color: #333;
  text-align: center;
  /* line-height: 160px; */
}
.el-menu-vertical-demo:not(.el-menu--collapse) {
  width: 200px;
  min-height: 400px;
}
</style>