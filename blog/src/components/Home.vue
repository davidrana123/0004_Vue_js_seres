<template>
<h1>Simple Form</h1>
<p>
    {{form}}
</p>
<form>
    <label>Email : </label>
    <input type="text" placeholder="Enter Email" v-model="form.email" />
    <br /><br />

    <label>Password : </label>
    <input type="password" placeholder="Enter Password" v-model="form.password" />
    <br /><br />
    <select v-model="form.country">
      <option>India</option>
       <option>China</option>
        <option>USA</option>  
    </select>
     <br /><br />
    <h3>Technology</h3>
     <label>Java : </label>
    <input type="checkbox" value="java"  v-model="form.technology" />
    <br /><br />
     <label>.Net : </label>
    <input type="checkbox" value=".net" v-model="form.technology" />
    <br /><br />
     <h3>Gender</h3>
     <label>Male : </label>
    <input type="radio" value="male" name="gender"  v-model="form.gender" />
    <br /><br />
     <label>Female : </label>
    <input type="radio" value="female" name="gender" v-model="form.gender" />
    <br /><br />


    <button v-on:click="login" type="button">Login</button>
</form>
</template>

<script>
export default {
    name: 'Home',
    data() {
        return {
            form: {
                email: '',
                password: '',
                country: '',
                technology: [],
                gender: ''
            }
        }
    },
    methods: {
        login() {
            console.warn("login data", this.form)
        }
    }

}
</script>

<style scoped>
h1 {
    color: orange;
}
</style>
