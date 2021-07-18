<template>
    <div class="footer">
        <p>Copyright &copy; 2021 maanpark.com All rights reserved.</p>
        <span v-if="isShowIcp">
            <a href="http://beian.miit.gov.cn/" target="_blank">辽 ICP 备 15008230 号</a>
        </span>
    </div>
</template>

<script>
export default {
    name: 'PageFooter',
    props: {
        isShowIcp: {
            type: [Boolean, Number],
            default: true
        }
    }
}
</script>

<style lang="less">
.footer {
    position: absolute;
    top: 100%;
    width: 100%;
    height: 50px;
}
</style>