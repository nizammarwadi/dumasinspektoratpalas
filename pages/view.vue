<template>
<div class="container-card">
    <div class="card card-detail" style="width: 64rem; height: auto; margin: auto; padding-top: 2rem;">
        <img :src="dataArticles.urlToImage" class="card-img-top" alt="#">
        <div class="card-body mt-3">
            <h3 class="card-title">
                {{ dataArticles.title }}
            </h3>
            <p class="card-text">
                {{ dataArticles.description }}
            </p>
            <p class="card-text">
                {{ dataArticles.content }}
            </p>
            <p class="card-text">
                Sumber: 
                <a href=":dataArticles.url">{{ dataArticles.url }}</a>
            </p>
        </div>
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
    width: 90%;
    margin-left: 5%;
    padding: 0 20px;
}
.card-detail {
    width: 60%;
}
.card-title {
    padding: 0 20px;
    font-weight: 700;
    font-size: 24px!important;
    text-align: center;
}
.card-text {
    padding:0 20px;
    margin-top: 30px;
}
@media(max-width: 600px) {
    .card-detail {
        width: 90%!important;
    }
    .card-img-top {
        margin-left: 0;
        width: 100%;
    }
}
</style>