<template>
    <div class="results">
        <p>Reaction time is: {{ score }} ms</p>
        <br>
        <p class="rank">Reflex rating: {{ rank }}</p>
    </div>
</template>

<script>
export default {
    props: ['score'],
    data() {
        return {
            rank: null
        }
    },
    mounted() {
        if (this.score < 250) {
            this.rank = 'Ninja fingers'
        } else if (this.score < 400) {
            this.rank = 'Rapid reflexes'
        } else {
            this.rank = 'Slow'
        }
    }
}
</script>

<style>
    .results {
    width: 300px;
    border-radius: 20px;
    background: #07b1f5;
    color: black;
    padding: 25px 0;
    margin: 40px auto;
    border: rgb(0, 89, 255) solid;
}
.rank {
    font-size: 1em;
    color: #18886c;
    font-weight: bold;
}
</style>