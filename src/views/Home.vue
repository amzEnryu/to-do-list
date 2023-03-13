<script>
import Header from '../components/Header.vue';
import Todo from '../components/Todo.vue';
import Footer from '../components/Footer.vue';
import { RouterLink, RouterView } from 'vue-router'
export default {
    name: 'Home',
    components: {
        Header,
        Todo,
        Footer
    },
}
</script>

<template>
    <Header></Header>
    <Todo></Todo>
    <Footer></Footer>
</template>
<style></style>

