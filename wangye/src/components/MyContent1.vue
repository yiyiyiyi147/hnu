<template>
    <div>
        <div class="p1">
            <img src="../assets/img-lab@2x.png" style="height: 370px;" />
        </div>

        <div class="l2">
            <h1>高级Web编程实验室</h1>
            <p>每个拥有自己完全独立的编程实验室，内置所有基础软件及学习素材。打开浏览器，即刻开始编程！</p>
            <button class="button4" @click="show2">了解详情</button>

        </div>
    </div>
</template>
<style>
    .l2 {
        margin: 30px;
        margin-left: 70px;
    }

    .p1 {
        height: 450px;
        text-align: center;
    }

    .button4 {
        cursor: pointer;
        width: 200px;
        height: 40px;
        padding: 10px;
    }

    .l2 h1 {
        padding: 10px;
    }

    .l2 p {
        padding: 10px;
    }
</style>
<script>
    export default {
        methods: {
            show2() {
                alert('了解详情')
            }
        }
    }

</script>