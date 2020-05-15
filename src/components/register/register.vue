<template>
    <div>
        Register
        <!-- <header/> -->
        <el-form :model='loginData' label-width="80px">
            <el-row>
                <el-col :span="8"><div class='place'></div></el-col>
                <el-col :span="8">
                    <el-form-item label="用户名">
                        <el-input placeholder="请输入用户名" v-model="loginData.userName"></el-input>
                    </el-form-item>
                </el-col>
                <el-col :span="8" class='place'><div></div></el-col>
            </el-row>
            <el-row>
                <el-col :span="8" class='place'><div></div></el-col>
                <el-col :span="8">
                    <el-form-item label="密码">
                        <el-input placeholder="请输入密码" v-model="loginData.password" show-password></el-input>
                    </el-form-item>
                </el-col>
                <el-col :span="8" class='place'><div></div></el-col>
            </el-row>
            <el-row>
                <el-col :span="8" class='place'><div></div></el-col>
                <el-col :span="8">
                    <el-form-item label="确认密码">
                        <el-input placeholder="请再次输入密码" v-model="loginData.checkPassword" show-password></el-input>
                    </el-form-item>
                </el-col>
                <el-col :span="8" class='place'><div></div></el-col>
            </el-row>
        </el-form>
        <el-row>
            <el-col :span="8" class='place'></el-col>
            <el-col :span="8">
                <el-button type="primary">注册</el-button>
                <el-button @click="toLogin">使用已有账号登陆</el-button>
            </el-col>
            <el-col :span="8" class='place'></el-col>
        </el-row>
    </div>
</template>

<script>
    // import header from '../header/header'

    export default {
        
        components: {
            // header,
        },
        data(){
            return {
                loginData:{
                    userName:'',
                    password:''
                }
            }
        },
        methods:{
            toLogin(){
                this.$router.push('/login')
            },
        }
    }
</script>
<style lang="less">
    .place{
        min-height :36px;
    }
</style>