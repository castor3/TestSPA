<template>
	<div id="centeredLogin">
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
</template>

<script>
import element from "element-ui";
import "element-ui/lib/theme-chalk/index.css";

export default {
  name: "Login",
  components: {
    // Login
    "el-form": element.Form,
    "el-form-item": element.FormItem,
    "el-input": element.Input,

    "el-button": element.Button
  },
  data() {
    return {
      testProperty: "",
      username: ""
    };
  },
  methods: {
    onSubmit() {
      console.log("submit!");
    }
  }
};
</script>

<style>

</style>
