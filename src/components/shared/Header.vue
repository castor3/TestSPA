<template>
		<!-- Header -->
		<el-header style="font-size: 12px">
			<span style="float: left">
				<el-col>
					<el-button @click="toggleIsCollapsed" size="mini" round>Menu</el-button>
				</el-col>
			</span>
			<span id="title">
				&lt;WebsiteName&gt;
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
    "el-button": element.Button
  },
  data() {
    return {
      isCollapsed: true,
		}
	},
  props: ["collapsed"],
  methods: {
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
.el-col {
  border-radius: 4px;
}
#title {
  font-size: 14px;
  font-weight: bold;
}
</style>
