<script>
export default {
    name: "AppMain",
    data() {
        return {

        }
    }
}
</script>

<template>
    <div class="main-body">
        <select class="form-select" aria-label="Default select example">
            <option value="1">Alien</option>
            <option value="2">Two</option>
            <option value="3">Three</option>
        </select>
        <div class="container-card">
            <div class="black-bar">Found 39 cards</div>
            1
        </div>
    </div>
</template>

<style scoped>
.main-body {
    height: 170vh;
    background-color: #D48F38;
    padding: 2rem;

}

.container-card {
    background-color: white;
    color: black;
    margin: 0 auto;
    width: calc(100% - 30rem);
    height: 150vh;
    padding: 2rem;
}

.form-select {
    width: 8rem;
    position: relative;
    left: 15rem;
    margin-bottom: 2rem;
}

.black-bar {
    width: calc(100% -);
    background-color: black;
    margin: 0 auto;
    height: 3rem;
    color: white;
    display: flex;
    align-items: center;
    font-weight: 600;
    padding-left: 0.5rem;

}
</style>
