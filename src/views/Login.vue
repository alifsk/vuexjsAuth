<template>
    <div id="login" class="login">
        <h1>Vue App Authentication</h1>
        <form class="">
        <div class="form-group">
            <input type="text" class="form-control" name="username" v-model="input.username" placeholder="Username" />
        </div>
        <div class="form-group">
            <input type="password" class="form-control" name="password" v-model="input.password" placeholder="Password" />
        </div>
        <button type="button" class="btn" v-on:click="login()">Login</button>
        </form>
    </div>
</template>

<script>
    export default {
        name: 'Login',
        data() {
            return {
                input: {
                    username: "",
                    password: ""
                }
            }
        },
        methods: {
            login() {
                if(this.input.username != "" && this.input.password != "") {
                    if(this.input.username == this.$parent.mockAccount.username && this.input.password == this.$parent.mockAccount.password) {
                        this.$emit("authenticated", true);
                        this.$router.replace({ name: "Secure" });
                    } else {
                        console.log("The username and / or password is incorrect");
                    }
                } else {
                    console.log("A username and password must be present");
                }
            }
        }
    }
</script>

<style scoped>
    #login {
        width: 500px;
        border: 1px solid #CCCCCC;
        background-color:#8AD0D6;
        margin: auto;
        margin-top: 150px;
        padding: 20px;
    }
    .h1{
        margin-bottom: 200px;
    }
    .login{
        border: 0px;
        border-radius: 20px;
    }
    .btn {
        background-color: #080f8a;
        color: #fff;
        border: 0px;
        border-radius: 60px;
        text-align: center;
        margin: 5px 2px;
        padding: 20px 15px;
        cursor: pointer;
        transition: 0.3s;
        margin: 20px;
        width: 300px;
    }
    .btn:hover {
        background-color: transparent;
        border: 2px solid #080f8a;
        color: #080f8a;
    }
</style>