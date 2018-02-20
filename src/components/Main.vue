<template>
	<div style="width:100%">
		<!-- Header -->
		<el-header style="font-size: 12px">
			<span style="float: left">
				<el-col>
					<el-button @click="toggleIsCollapsed" size="mini" round>Menu</el-button>
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
					<span>Rui</span>
				</el-col>
			</span>
		</el-header>

		<!-- Main content -->
		<el-main>
			<div id="centerLogin">
				<h1>Login</h1>
				<el-form>
					<el-form-item>
						<el-input placeholder="username" v-model="username"></el-input>
					</el-form-item>
					<el-form-item>
						<el-input type="password" placeholder="password"></el-input>
					</el-form-item>
					<el-form-item>
						<el-button @click="onSubmit" type="primary">Login</el-button>
					</el-form-item>
				</el-form>
			</div>
		</el-main>
	</div>
</template>

<script>
import element from "element-ui";
import "element-ui/lib/theme-chalk/index.css";

export default {
  name: "Header",
  components: {
    // Header
    "el-header": element.Header,
    "el-dropdown": element.Dropdown,
    "el-dropdown-menu": element.DropdownMenu,
    "el-dropdown-item": element.DropdownItem,
    "el-col": element.Col,

    // Main
    "el-main": element.Main,
    "el-form": element.Form,
    "el-form-item": element.FormItem,
    "el-input": element.Input,

    "el-button": element.Button
  },
  data() {
    return {
      isCollapsed: true,
      testProperty: "",
      username: ""
    };
  },
  props: ["collapseValue"],
  methods: {
    onSubmit() {
      console.log("submit!");
    },
    toggleIsCollapsed() {
      this.isCollapsed = !this.isCollapsed;
      this.$emit("collapseChanged", this.isCollapsed);
      console.log("Menu is collapsed = " + this.isCollapsed);
    }
  }
};
</script>

<style>
#centerLogin {
  width: 25%;
  margin: 0 auto;
}
.el-header {
  background-color: #b3c0d1;
  color: #333;
  text-align: center;
  line-height: 60px;
}
.el-col {
  border-radius: 4px;
}
.el-main {
  background-color: #e9eef3;
  color: #333;
  text-align: center;
}
</style>
