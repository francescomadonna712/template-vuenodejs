<script>
import AppCard from "./AppCard.vue";

export default {
    components: {
        AppCard,
    },
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

        <AppCard />
    </div>



</template>

<style scoped>
.card-cnt {
    display: flex;
    flex-direction: row;
    flex-wrap: wrap;

}

.main-body {

    background-color: #D48F38;
    padding: 2rem;

}

.cnt {
    background-color: white;
    width: 80%;
    margin: 0 auto;
}

.form-select {
    width: 8rem;
    position: relative;
    left: 1rem;
    margin-bottom: 2rem;
}

.black-bar {
    width: 100%;
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
