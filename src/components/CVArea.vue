<template>
    <div class="container">
        <div style="display:flex; align-content: space-between">
            <h3>{{name}}</h3>
            <v-icon style="margin-left: 7px">{{icon}}</v-icon>
        </div>
        <div class="field" v-for="field in fields"  v-bind:key="field">
            <p>{{field}}</p>
        </div>
    </div>
</template>

<script>
    export default {
        name: "CVArea",

        props: {
            name: String,
            fields: [],
            icon: String
        },
    }
</script>

<style scoped>
    .container {
        text-align: left;
        padding: 20px 20px;
        background-color: white;
        border-radius: 10px;
        margin: 13px;
        width: 70%;
        align-self: center;
    }

    .field {
        border-top: 2px solid lightgray;
        margin-top: 10px;
        padding-top: 10px;
    }


    @media screen and (max-width: 800px) {
        .container {
            width: 90%;
        }
    }
</style>