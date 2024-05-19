<template>
    <div>
        <div class="p2">
            <img src="../assets/img-screens@2x.png" style="height: 380px;width: 420px;">
        </div>
        <div class="l3">
            <h1>双屏学习</h1>
            <p>双屏学习，小屏视频互动，大屏实际操作，学习无障碍。打开浏览器，即刻开始编程！</p>
            <button class="button5" @click="show3">了解详情</button>
        </div>
    </div>
</template>
<style>
    .p2 {
        text-align: center;
        height: 380px;
    }

    .l3 {
        margin: 70px;
        margin-left: 70px;
    }

    .button5 {
        cursor: pointer;
        width: 200px;
        height: 40px;
        padding: 10px;
    }

    .l3 h1 {
        padding: 10px;
    }

    .l3 p {
        padding: 10px;
    }
</style>
<script>
    export default {
        methods: {
            show3() {
                alert('了解详情')
            }
        }
    }

</script>