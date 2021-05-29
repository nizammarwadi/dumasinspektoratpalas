<template>
    <div class="container">
        <div class="row justify-content-start">
            <div class="col">
                <div v-for="(item, index) in dataArticles" :key="index" class="card-content">
                    <Card
                    :urlToImage="item.urlToImage"
                    :cardTitle="item.title"
                    :cardDescription="item.description"
                    @card-click="openNews(item)"
                    />
                </div> 
            </div>
        </div>
    </div>     
</template>

<script>
import axios from 'axios'
import Card from '~/components/organisms/Card.vue'
export default {
    components: {
        Card: Card,
    },
    props:  {
        Card: Card,
    },
    data() {
        return {
            dataArticles: [],
            articles: [],
        };
    },
    mounted() {
        this.getDataArticles();
        },
    methods: {
        async getDataArticles() {
            const articles = await axios.get(`https://beritaku-api.herokuapp.com/articles`)
            console.log(articles)
            this.dataArticles = articles.data
    },
    openNews(item) {
            this.$router.push(`/view?id=${item.id}`)
        }
    },
};
</script>

<style>
.card-content {
    display: inline-block;
}
.col {
    text-align: center;
}
</style>