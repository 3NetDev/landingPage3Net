<template>
    <div>
        <Header/>
        <Form/>
        <Footer/>
    </div>
</template>

<script>
import Header from '~/components/Header.vue';
import Footer from '~/components/Footer.vue';
import Form from '../components/Form.vue';
export default {
    components: { Header, Footer, Form }
}
</script>

<style>

</style>