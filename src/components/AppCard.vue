<script>
import iMieiDati from '../data/store.js';
export default {
    name: "AppFooter",
    data() {
        return {
            iMieiDati

        }
    }
}
</script>

<template>
    <div class="cnt">
        <div class="black-bar">Found 10 card</div>
        <div v-for="card in iMieiDati.card" :key="card.name" class="card">
            <div v-for="image in card.card_images" :key="image.image_url" class="card-images">
                <img :src="image.image_url_small" alt="Small Card Image">
            </div>
            <h5 class="name">{{ card.name }}</h5>
            <p class="tipo">{{ card.archetype }}</p>


        </div>
    </div>
</template>

<style scoped>
.black-bar {
    width: 100%;
    background-color: black;
    height: 3rem;
    color: white;
    justify-content: center;
    font-weight: 600;
    padding-left: 0.5rem;
    align-items: center;

}

.card {

    color: white;
    display: flex;
    align-items: center;
    background-color: #D48F38;

    margin: 18px;
    width: 18rem;
}

.card-images img {
    display: block;
    height: 25rem;
    margin-bottom: 3rem;

}

.name {
    font-weight: bold;
}

.tipo {
    color: black;
}
</style>
