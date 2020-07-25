<template>
    <div class="container">
        <form @submit="submitSentence">
            <input type="text" class="form-control" v-model="sentence" name="sentence" placeholder="Type a sentence here...">
            <button class="btn btn-success mt-2">SUBMIT</button>
        </form>
    </div>
</template>

<script>
    export default {
        name: "SentenceInput",
        data() {
            return {
                sentence: ''
            }
        },
        methods: {
            submitSentence(e){
                e.preventDefault();
                const s = {
                    sentence: this.sentence,
                }
                this.$emit('submit-sentence', s);
                this.sentence = '';
            }
        }
    }
</script>

<style scoped>

</style>