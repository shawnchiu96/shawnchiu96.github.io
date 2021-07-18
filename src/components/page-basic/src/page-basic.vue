<template>
    <div>
        <page-navbar></page-navbar>
        <slot name="page-body"></slot>
        <page-footer></page-footer>
    </div>
</template>

<script>
import PageNavbar from '../../navbar-top'
import PageFooter from '../../footer'

export default {
    name: 'PageBasic',
    components: {
        PageNavbar,
        PageFooter
    }
}
</script>

<style lang="less">
.boxx {
    width: 100px;
    height: 100px;
    background-color: aquamarine;
}
</style>