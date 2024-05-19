<template>
    <div>
        <input type="checkbox" id="display1">
        <input type="checkbox" id="display2">
        <label for="display1" class="diaplay-login">登录</label>
        <label for="display2" class="diaplay-register">注册</label>

        <img src="../assets/logo-white.svg">

        <div class="l1">
            <h1>云端编程，浏览器里边学边练</h1>
            <p>软件定义一切，网络连接时空，学习软件技术，创造未来世界。</p>
            <button class="button3" @click="show1">马上学习</button>
        </div>
        <div class="login-container">
            <h2>登录</h2>
            <label for="display1" class="close1">&times;</label>
            <form action="http://localhost:8081/ " method="get">
                <label style="color: red;margin-left: 4%;margin-top: 1%;position: absolute;">*</label>
                <h3 style="margin-left: 7%;">用户名：</h3>
                <label style="color: red;margin-left: 4%;margin-top: 11%;position: absolute;">*</label>
                <input type="text" v-model="username" placeholder="请输入用户名">
                <h3 style="margin-left: 7%;">密码：</h3>
                <input type="password" v-model="password" placeholder="请输入密码">
                <input type="submit" value="登录" @click="login">
                <button type="reset">重置</button>
            </form>
        </div>
        <div class="register-container">
            <h2>注册</h2>
            <label for="display2" class="close2">&times;</label>
            <form action="http://localhost:8081/" method="get">
                <label style="color: red;margin-left: 4%;margin-top: 1%;position: absolute;">*</label>
                <h3 style="margin-left: 7%;">用户名：</h3>
                <input type="text" name="username" placeholder="请输入用户名">
                <label style="color: red;left: 8%;margin-top: 11%;position: absolute;">*</label>
                <h3 style="margin-left: 7%;">密码：</h3>
                <input type="password" name="password" placeholder="请输入密码">
                <input type="submit" value="注册">
                <button type="reset">重置</button>
            </form>
        </div>
    </div>
</template>

<style>
    input[type='checkbox'] {
        display: none;
    }

    #display1:checked~.login-container {
        display: block;
    }

    #display2:checked~.register-container {
        display: block;
    }

    .l1 {
        text-align: center;
        color: white;
        padding: 60px;

    }

    .button3 {
        cursor: pointer;
        width: 120px;
        height: 40px;
        margin-right: 5px;
        background-color: white;
        color: rgb(36, 144, 203);
        font-size: 20px;
        border: 1px solid white;
        margin: 40px;
    }

    .header img {
        margin: 20px;
    }

    .login-container {
        display: none;
        width: 500px;
        height: 300px;
        background-color: #fff;
        padding: 20px;
        border-radius: 8px;
        left: 50%;
        top: 50%;
        transform: translate(-50%, -50%);
        position: absolute;
        z-index: 999;
    }

    .login-container h2 {
        margin-bottom: 20px;
        text-align: center;
    }

    .close1,
    .close2 {
        position: absolute;
        right: 20px;
        top: 10px;
        font-size: 30px;
    }

    .login-container input[type="text"],
    .login-container input[type="password"] {
        width: 80%;
        padding: 10px;
        margin-bottom: 20px;
        margin-left: 7%;
        border: 1px solid #ccc;
        border-radius: 4px;
    }

    .login-container input[type="submit"] {
        position: absolute;
        width: 30%;
        bottom: 20%;
        left: 7%;
        padding: 10px;
        background-color: #007bff;
        color: #fff;
        border: none;
        border-radius: 4px;
        cursor: pointer;
        font-size: 15px;
    }

    .login-container button {
        position: absolute;
        width: 30%;
        bottom: 20%;
        left: 60%;
        padding: 10px;
        background-color: #007bff;
        color: #fff;
        border: none;
        border-radius: 4px;
        cursor: pointer;
        font-size: 15px;
    }

    .login-container input[type="submit"]:hover {
        background-color: #0056b3;
    }

    .register-container {
        display: none;
        width: 500px;
        height: 300px;
        background-color: #fff;
        padding: 20px;
        border-radius: 8px;
        left: 50%;
        top: 50%;
        transform: translate(-50%, -50%);
        position: absolute;
        z-index: 999;
    }

    .register-container h2 {
        margin-bottom: 20px;
        text-align: center;
    }

    .register-container h1 {
        margin-bottom: 20px;
        margin-right: 5px;
    }

    .register-container input[type="text"],
    .register-container input[type="password"] {
        width: 80%;
        padding: 10px;
        margin-bottom: 20px;
        margin-left: 7%;
        border: 1px solid #ccc;
        border-radius: 4px;
    }

    .register-container input[type="submit"] {
        position: absolute;
        width: 30%;
        bottom: 20%;
        left: 7%;
        padding: 10px;
        background-color: #007bff;
        color: #fff;
        border: none;
        border-radius: 4px;
        cursor: pointer;
        font-size: 15px;
    }

    .register-container button {
        position: absolute;
        width: 30%;
        bottom: 20%;
        left: 60%;
        padding: 10px;
        background-color: #007bff;
        color: #fff;
        border: none;
        border-radius: 4px;
        cursor: pointer;
        font-size: 15px;
    }

    .register-container input[type="submit"]:hover {
        background-color: #0056b3;
    }

    .diaplay-login {
        color: white;
        padding: 10px;
        position: absolute;
        right: 200px;
        top: 40px;
        border: 2px solid white;
        cursor: pointer;
        display: flex;
    }

    .diaplay-register {
        color: white;
        padding: 10px;
        position: absolute;
        right: 130px;
        top: 40px;
        border: 2px solid white;
        cursor: pointer;
        display: flex;
    }
</style>
<script>
    export default {
        data() {
            return {
                username: '',
                password: ''
            };
        },
        methods: {
            show1() {
                alert('马上学习')
            },
            login() {
                const axios = require('axios');
                axios.get('http://localhost:3000/users', {
                    username: this.username,
                    password: this.password
                })
                    .then((r) => {
                        if (r.data[0].username === this.username && r.data[0].password === this.password) {
                            alert("登陆成功")
                            setTimeout(() => {
                                this.$router.replace("App");
                            }, 10);
                        } else {
                            alert("用户名或密码错误")
                            this.username = ''
                            this.password = ''
                        }
                    })
                    .catch(error => {
                        console.log(error);
                    })
            },
            register() {
                const axios = require('axios');
                axios.get('http://localhost:3000/users', {
                    username: this.username,
                    password: this.password
                })
                    .then(respone => {
                        console.log(respone.data);

                    })
                    .catch(error => {
                        console.log(error);
                    });
            }
        }
    };
</script>