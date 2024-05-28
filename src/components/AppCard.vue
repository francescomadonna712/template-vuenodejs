<script>
import axios from 'axios';

export default {
    data() {
        return {
            cards: []
        };
    },
    created() {
        this.CardInfo();
    },
    methods: {
        CardInfo() {
            axios.get('https://db.ygoprodeck.com/api/v7/cardinfo.php?num=25&offset=0')
                .then(response => {
                    this.cards = response.data.data;
                })
        }
    }
};

</script>

<template>
    <div class="cnt">
        <div class="black-bar">Found 10 card</div>
        <div class="card-container">
            <div class="card" v-for="card in cards" :key="card.id">
                <img :src="card.card_images[0].image_url" :alt="card.name" class="card-image" />
                <h5 class="name">{{ card.name }}</h5>
                <p class="tipo">{{ card.archetype }}</p>
            </div>
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

.card-container {
    display: flex;
    justify-content: center;
    flex-direction: row;
    flex-wrap: wrap;
    width: 100%;
}

.card {

    color: white;
    display: flex;
    align-items: center;
    background-color: #D48F38;
    margin: 18px;
    width: 15rem;
}

.card-image {
    width: 200px;
    height: auto;

}

.name {
    padding-top: 1rem;
    text-align: center;
    font-weight: bold;
}

.tipo {
    color: black;
}

.list {
    list-style: none;
}
</style>
