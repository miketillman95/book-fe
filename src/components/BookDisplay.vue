<script setup>

</script>

<template>
    <h1>Welcome to the Book collection</h1>
    <div class="card-container">
        <div class="card text-dark bg-light mb-3"  v-for="book in books" :key="'book.id'" style="max-width: 18rem;">
            <div class="card-header">Book title:</div>
            <div class="card-body">
                <h5 class="card-title">Description:</h5>
                <!-- add description here -->
                <p class="card-text">
                    {{ book.title }}
                </p>
            </div>
        </div>
    </div>
</template>


<script>
import axios from 'axios'

export default {
    data(){
        return {
            books: []
        }
    },
    mounted(){
        this.fetchData()
    },
    methods:{
        fetchData(){
            axios.get('https://jsonplaceholder.typicode.com/todos')
                .then(res => {
                    this.books = res.data.slice(0,10)
                })
                .catch(error => {
                    console.log(error)
                })
        }
    }
}
</script>

<style>
.card-container {
    display: flex;
    flex-wrap: wrap;
    justify-content: space-between;
}
</style>