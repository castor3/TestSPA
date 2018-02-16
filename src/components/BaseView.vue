<template>
	<div>
		<!-- <h1>{{ msg }}</h1>
		<span v-bind:title="newThing">
			<h2>{{employee}}</h2>
		</span> -->
		<!-- <app-newfile></app-newfile> -->
		<!-- <elem-button @click="MethodToBeCalled">Click this</elem-button>-->


	</div>
</template>

<script>
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
  },
  data() {
    return {
      msg: "Welcome to Your Vue.js App",
      insideMessage: "You loaded this page on " + new Date().toLocaleString(),
      newThing: "This is the employee's name",
      employee: "Rui Santos"
    };
  },
  methods: {
    MethodToBeCalled: function() {
      alert("This is the employee's name: Rui Santos");
    }
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
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
