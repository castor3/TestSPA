<template>
	<div style="width:100%">
		<el-header style="font-size: 12px">
			<el-row>
				<span style="float: left">
					<el-col>
						<!-- Collapse / Expand buttons -->
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
			</el-row>
		</el-header>

		<!-- Main content -->
		<el-main>
			<h1>Main content</h1>
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
    "el-radio-group": element.RadioGroup,
    "el-radio-button": element.RadioButton,
    "el-row": element.Row,
    "el-col": element.Col,
    "el-main": element.Main,
    "el-button": element.Button
  },
  data() {
    return {
      isCollapsed: true,
      testProperty: ""
    };
  },
  props: ["collapseValue"],
  methods: {
    buttonClicked() {
      alert("mensagem");
      this.testProperty = "newValue";
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
.el-header {
  background-color: #b3c0d1;
  color: #333;
  text-align: center;
  line-height: 60px;
}
.el-row {
  margin-bottom: 20px;
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
