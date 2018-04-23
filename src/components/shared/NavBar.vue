<template>
	<el-menu class="el-menu-vertical-demo" @open="handleOpen" @close="handleClose" :collapse="collapsed">
		<!-- Main window -->
		<el-menu-item index="1">
			<i class="el-icon-message"></i>
			<span slot="title">
				<el-button @click="homeClicked">{{collapsed}}</el-button>
			</span>
		</el-menu-item>
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
		<el-menu-item index="3">
			<i class="el-icon-location"></i>
			<span slot="title">Fields</span>
		</el-menu-item>
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
</template>


<script>
import element from "element-ui";
import "element-ui/lib/theme-chalk/index.css";

export default {
  name: "NavBar",
  components: {
    // NavBar
    "el-menu": element.Menu,
    "el-submenu": element.Submenu,
    "el-menu-item-group": element.MenuItemGroup,
    "el-menu-item": element.MenuItem,
    "el-button": element.Button
  },
  data() {
    return {
      
		}
	},
  props: ["collapsed"],
  methods: {
    handleOpen(key, keyPath) {
      console.log(key, keyPath);
    },
    handleClose(key, keyPath) {
      console.log(key, keyPath);
    },
    homeClicked() {
      console.log("click");
    }
  }
};
</script>


<style>

</style>
