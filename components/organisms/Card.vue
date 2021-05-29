<template>
    <div class="container">
        <div class="card" style="width: 18rem; height: auto">
            <img :src="urlToImage" class="card-img-top" alt="#">
            <div class="card-body">
                <h3 class="card-title">
                    {{ cardTitle }}
                </h3>
                <h4 class="card-date">
                    {{ cardDescription }}
                </h4>
                <p class="card-text">
                    {{ cardContent }}
                </p>
                <a :href="cardUrl" class="btn btn-primary" @click="$emit('card-click')">Click For More</a>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    props: {
        urlToImage: "",
        cardTitle: "",
        cardUrl: "",
        cardDescription: "",
        cardContent: ""
    }
}
</script>

<style>
.card {
  width: auto;
  height: 26rem;
  font-family: sans-serif;
  padding: 8px;
}
.card-body {
    text-align: justify!important;
    padding: 4px!important;
}
.btn {
    height: 30px;
    font-size: small;
    margin: 10px

}
.card-title {
    padding: 0px 10px;
    font-weight: 700;
    font-size: medium;
    margin-top: 30px;
}
.card-text {
    margin: 10px;
}
.card-date {
    padding: 0px 10px;
    font-style: italic;
    font-size: small;
    
}
</style>