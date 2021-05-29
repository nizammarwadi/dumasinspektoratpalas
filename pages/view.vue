<template>
  <div class="card" style="width: 64rem; height: auto; margin: auto; padding-top: 2rem;">
        <img :src="dataArticles.urlToImage" class="card-img-top" alt="#">
        <div class="card-body">
            <h3 class="card-title">
                {{ dataArticles.title }}
            </h3>
            <p class="card-text">
                {{ dataArticles.description }}
            </p>
            <p class="card-text">
                {{ dataArticles.content }}
            </p>
        </div>
    </div>
</template>

<script>
import axios from 'axios'
export default {
    data() {
        return {
            dataArticles: {},
            idArticles: 0
        }     
    },
    mounted() {
        this.idArticles = this.$route.query.id
        this.getCurrentNews()
    },
    methods: {
        async getCurrentNews() {
            const articles = await axios.get(`https://beritaku-api.herokuapp.com/articles/${this.idArticles}`)
            this.dataArticles = articles.data
            console.log(this.dataArticles)
        }
    }
}
</script>

<style>
.card-img-top {
    width: 42rem;
    margin-left: 170px;
}
.card-title {
    padding: 20px;
    font-weight: 700;
    font-size: 18px!important;
    text-align: center;
}
.card-text {
    padding: 20px;
}
</style>