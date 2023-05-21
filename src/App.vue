<template>
    <div class="app">

    <button @click="fetchData">GET</button>
    <input v-model="url" placeholder="url"> 
    <!--
    <ul>
        <li v-for="item in data" :key="item.id">
            {{ item }}
        </li>
    </ul>
    -->

    </div>
</template>

<script>
export default {
    data() {
        return {
            url: "",
            data: [],
        }
    },  

    methods: {
        fetchData() {
            fetch(this.url)
                .then(r => alert(r))
                //.then(response => response.json())
                //.then(data => {this.data = data;})
                .catch(error => {console.error("Error, ", error);})
        },
    }
}
</script>

<style>
body {
    background-color: #181818;
}
.app {
    background-color: #222;
    color: #eee;
    }
button {
    background-color: #474;
    color: #eee;
    border: solid #353;
}
button:hover {
    background-color: #585;
}
</style>

