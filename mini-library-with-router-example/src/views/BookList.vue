<template>
    <div>
        <main class="books">
            <Book v-for="(book, index) in books" v-bind:key="index" 
            v-bind:book="book"></Book>
        </main>
    </div>
</template>

<script>
import Book from '../components/Book';

export default {
    name: 'BookList',
    components: {
        Book
    },
    props: {
        books: Array
    }
}
</script>

<style>
    .books {
        display: grid;
        gap: 1rem;
        grid-template-columns: repeat(4, 1fr);
    }
</style>