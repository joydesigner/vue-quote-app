<template>
    <div class="row">
        <form action="">
            <div class="col-sm-8 col-sm-offset-2 col-xs-12 col-md-6 col-md-offset-3">
                <label for="quote">Quote</label>  
                <textarea name="" id="quote" cols="120" rows="1" class="form-control" v-model="quote"></textarea>
            </div>
            <div class="col-sm-8 col-sm-offset-2 col-xs-12 col-md-6 col-md-offset-3">
                <button class="btn btn-primary quote-btn" @click.prevent="createNew">Add quote</button>
            </div>
        </form>
    </div>
</template>

<script>
export default {
    data() {
        return {
            quote: ''
        }
    },
    methods: {
        createNew() {
            this.$emit('quoteAdded', this.quote);
            this.quote = '';
        }
    },
}
</script>

<style lang="scss">
    .quote-btn {
        margin-top: 20px;
    }
</style>
