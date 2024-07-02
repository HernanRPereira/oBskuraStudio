<template>
    <div class="HeaderComponent">
        <img :src="logo" alt="LOGO">
        <h1>OBSKURA<br>STUDIO</h1>
    </div>
</template>

<script>
import logo from '@/assets/logo.png'

export default {
    data() {
        return {
            logo
        }
    },
};

</script>

<style>
.HeaderComponent{
    display: flex;
    justify-content: center;
    align-items: center;
}
.HeaderComponent img{
    width: 5vw;
    height: auto;
}
</style>