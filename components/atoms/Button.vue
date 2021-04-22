<template>
   <div class="container">
       <button class="button btn btn-primary" @click.prevent="$emit ('click-button')">{{titleButton}}</button>
   </div>
</template>

<script>
export default {
    props: {
        titleButton: {
            type: String,
            default: 'Submit'
        }
    }

}
</script>

<style>

</style>