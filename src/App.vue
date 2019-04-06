<template>

   <div class="container">
    <app-new-quote @quoteAdded="newQuote"></app-new-quote>
    <app-quote-grid :quotes="quotes" @quoteDeleted = "deleteQuote"></app-quote-grid>
    <div class="row alert-row">
      <div class="col-sm-12 text-center">
        <div class="alert alert-info">
          Click on a quote to delete it!
        </div>
      </div>
    </div>
   </div>
</template>

<script>
import QuoteGrid from './components/QuoteGrid.vue';
import NewQuote from './components/NewQuote.vue';
export default {
  name: 'app',
  data() {
    return {
      quotes: [
        'Just a Quote to see'
      ],
      maxQuotes: 10
    }
  },
  components: {
    appQuoteGrid: QuoteGrid,
    appNewQuote: NewQuote
  },
  methods: {
    newQuote(quote) {
      this.quotes.push(quote);
    },
    deleteQuote(index) {
      this.quotes.splice(index, 1);
    }
  },  
}
</script>

<style lang='scss'>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
 
}
 .alert-row {
    margin-top: 15px;
  }
</style>
