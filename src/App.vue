<template>
    <div class="app">

    <button @click="fetchData">GET</button>
    <ul>
        <li v-for="item in data" :key="item.id">
            {{ item }}
        </li>
    </ul>

    </div>
</template>

<script>
export default {
    data() {
        return {
            data: [],
        }
    },  

    methods: {
        fetchData() {
            fetch("https://jsonplaceholder.typicode.com/todos")
                .then(response => response.json())
                .then(data => {this.data = data;})
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

