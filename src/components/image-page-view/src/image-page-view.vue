<template>
    <div class="image-page bg-image">
        <div class="image-page__content bg-blur">
            <h2 v-if="title">{{ title }}</h2>
            <p v-if="content">{{ content }}</p>
        </div>
    </div>
</template>

<script>
export default {
    name: 'ImagePageView',
    props: {
        title: {
            type: String,
            default: ''
        },

        content: {
            type: String,
            default: ''
        }
    }
}
</script>

<style lang="less">
.image-page {
    position: absolute;
    top: 0;
    bottom: 0;
    width: 100%;
    height: 100%;

    &__content {
        position: relative;
        width: 100%;
        height: 100%;
        display: flex;
        justify-content: center;
        align-items: center;
        flex-direction: column;
    }
}

.bg-image {
    background-image: url('https://images.unsplash.com/photo-1589111487049-028898f487e8');
    background-size: cover;
    background-position: center;
    background-color: #f8f8f8;
}

.light-mode .bg-blur {
    background-color: rgba(255, 255, 255, 0.5);
    backdrop-filter: saturate(150%) blur(20px);
    -webkit-backdrop-filter: saturate(150%) blur(20px);
}

.dark-mode .bg-blur {
    color: #ffffff;
    background-color: rgba(0, 0, 0, 0.5);
    backdrop-filter: saturate(150%) blur(20px);
    -webkit-backdrop-filter: saturate(150%) blur(20px);
}
</style>