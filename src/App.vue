<template>
   <div class="container">
     <app-progress-bar :qoutes="quotes" :maxQuotes="maxQuotes"></app-progress-bar>
     <app-new-quote @quoteAdded="newQuote"></app-new-quote>
     <app-quote-grind :qoutes="quotes" @quoteDeleted="deleteQuote"></app-quote-grind>
     <div class="row">
       <div class="col col-md-12 text-center">
         <div class="alert alert-info">info: Click on a Quote to delete it!</div>
       </div>
     </div>
    </div>
</template>

<script>
import QuoteGrind from "./components/QuoteGrid.vue";
import NewQuote from "./components/NewQuote.vue";
import ProgressBar from "./components/ProgressBar.vue";
export default {
  name: "app",
  data() {
    return {
      quotes: ["Just a Quote to see something"],
      maxQuotes: 10
    };
  },
  methods: {
    newQuote(quote) {
      if (this.quotes.length < this.maxQuotes) {
        this.quotes.push(quote);
      }else{
        alert('Please delete quotes first');
      }
    },
    deleteQuote(index) {
      this.quotes.splice(index, 1);
    }
  },
  components: {
    appQuoteGrind: QuoteGrind,
    appNewQuote: NewQuote,
    appProgressBar: ProgressBar
  }
};
</script>

<style lang="scss">

</style>
