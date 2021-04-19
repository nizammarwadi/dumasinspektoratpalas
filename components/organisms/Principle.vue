<template>
    <section class="principle">
        <div class="principle-left">
            <div>
                <h3>Ayo ikut serta berpartisipasi dalam menegakkan keadilan untuk masyarakat yang lebih baik </h3>
                <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Inventore maxime quam numquam recusandae distinctio. Officia nam totam laboriosam unde provident nihil, excepturi esse ipsa quisquam velit autem fugiat libero reprehenderit. </p>
                <button class="btn btn-primary"> Fast Response</button>
            </div>
        </div>
        <div class="principle-middle mr-2">
            <img src="~/assets/images/laptop.jpg" width="250px" height="450px" alt="not found">
        </div>
          <div class="principle-right">
            <img src="~/assets/images/dpr.jpg" width="200px" height="330px" alt="not found">
        </div>
    </section>
</template>

<script>
export default {

}
</script>

<style>
    .principle {
        display: flex;
        align-items: center;
        justify-content: center;
        margin-bottom: 150px;
    }
    .principle-left {
        max-width: 550px;
        background-color: rgb(245, 246, 247);
        padding: 20px 20px;
        position: relative;
        margin-right: -40px;
        box-shadow: 10px 10px 5px white;
        opacity: .9;
    }
    .principle-left h3 {
        font-weight: 700;
    }
    .principle-middle img {
        object-fit: cover;
        /* opacity: .9; */
    }
    .principle-right img {
        object-fit: cover;
    }

</style>