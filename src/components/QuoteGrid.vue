<template>
    <div class="row">
        <app-quote v-for="(qoute, index) in qoutes" :key="qoute" @click.native="deleteQuote(index)">{{ qoute }}</app-quote>
    </div>
</template>

<script>
import Quote from './Quote.vue';
export default {
    props: ['qoutes'],
    methods: {
        deleteQuote(index){
             this.$emit('quoteDeleted', index);
        }
    },
    components: {
        appQuote: Quote
    }
}
</script>
<style>

</style>
