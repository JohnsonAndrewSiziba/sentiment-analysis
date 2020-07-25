<template>
    <div class="container mt-2 text-left">
        <p class="text-success">
            {{results.s}}
        </p>
        <table class="table w-50 text-secondary">
            <tr>
                <td>Positive Score</td>
                <td>{{results.pos}}%</td>
            </tr>
            <tr>
                <td>Negative Score</td>
                <td>{{results.neg}}%</td>
            </tr>
            <tr>
                <td>Neutral Score</td>
                <td>{{results.neu}}%</td>
            </tr>
            <tr>
                <td>Overall</td>
                <td>{{results.ova}}</td>
            </tr>


        </table>
    </div>
</template>

<script>
    export default {
        name: "Results",
        props: ["results"]
    }
</script>

<style scoped>

</style>