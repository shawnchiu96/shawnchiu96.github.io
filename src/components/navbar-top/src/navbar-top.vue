<template>
    <div class="navbar">
        <ul class="navbar__links">
            <li v-for="nav in navLinks" :key="nav._id" class="navbar__links--item">
                <a href="#">{{ nav.text }}</a>
            </li>
        </ul>
    </div>
</template>

<script>
export default {
    name: 'PageNavbar',
    data() {
        const navLinks = [{
            _id: 0,
            text: '首页',
            url: '#'
        }, {
            _id: 1,
            text: '关于',
            url: '#'
        }]
        return {
            navLinks
        }
    }
}
</script>

<style lang="less">
.navbar {
    position: fixed;
    width: 100%;
    height: 80px;
    background-color: rgba(0, 0, 0, 0.5);
    z-index: 1000;

    &__links {
        margin: 0;
        padding: 5px 15px;
        display: flex;
        justify-content: center;
        align-items: center;
        list-style-type: none;

        &--item {
            width: 80px;
        }
    }

    a {
        color: #fff;
        text-decoration: none;
    }

    a:hover {
        color: #1976d2;
    }
}
</style>