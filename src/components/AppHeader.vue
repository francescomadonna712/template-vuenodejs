<script>
export default {
    name: "AppHeader",
    data() {
        return {


        }
    }
}
</script>

<template>
    <div class="header">
        <div class="logo"><img src="../assets/Logo.jpg" alt=""></div>
        <div class="title">
            <h1>Yu-Gi-Oh Api</h1>
        </div>
    </div>
</template>

<style scoped>
.header {
    width: 100%;
    color: black;
    background-color: white;
    display: flex;
    flex-direction: row;
    align-items: center;
}

.logo {
    display: flex;
    width: 120px;
    height: 100px;
    align-items: center;
}

.logo img {
    width: 100px;
    height: 50px;
}
</style>
