<template>
    <div class="header">
        <el-menu :default-active="activeIndex" class="el-menu-demo" mode="horizontal" @select="handleSelect" background-color="#545c64" text-color="#fff" active-text-color="#ffd04b">
            <a class="head">
                Coder YU
            </a>
            <el-menu-item index="1" @click="gohome">网站首页</el-menu-item>
            <el-menu-item index="2" @click="goarticle">文章专栏</el-menu-item>
            <el-menu-item index="3" @click="golife">生活点滴</el-menu-item>
            <el-menu-item index="4" @click="goabout">关于本站</el-menu-item>
        </el-menu>
    </div>
</template>
<script>
export default {
    name: "header0",
    data() {
        return {
            activeIndex: "1"
        };
    },
    methods: {
        handleSelect(key, keyPath) {},
        gohome() {
            this.$router.push("/");
        },
        goarticle() {
            this.$router.push("/articles");
        },
        golife() {
            this.$router.push("/life");
        },
        goabout() {
            this.$router.push("/about");
        }
    }
};
</script>

<style>
a {
    cursor: pointer;
}
.el-menu .el-menu-item {
    font-size: 18px;
    display: inline-block;
}
.el-menu {
    text-align: right;
    padding-right: 20px;
}
.header .el-menu--horizontal > .el-menu-item {
    float: none;
    height: auto;
    line-height: 25px;
    padding: 15px 30px 15px 30px;
}
.head {
    color: white;
    font-size: 28px;
    vertical-align: center;
    left: 5%;
    top: 24%;
    position: absolute;
    letter-spacing: 2px;
}
@media screen and (max-width: 426px) {
    .header .el-menu--horizontal > .el-menu-item {
        font-size: 14px;
        padding: 5px;
    }
    .el-menu {
        padding-right: 0px;
    }
    .head {
        font-size: 14px;
        top: 25%;
    }
}
@media screen and (max-width: 376px) {
    .header .el-menu--horizontal > .el-menu-item {
        font-size: 12px;
        padding: 3px;
    }
}
</style>