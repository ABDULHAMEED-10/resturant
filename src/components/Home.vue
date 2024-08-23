<template>
    <div>

        <input type="text" placeholder="name" v-model="name">
        <br />
        <br />
        <input type="text" placeholder="email" v-model="email">
        <br />
        <br />
        <button v-on:click="submit" type="button">Submit</button>

    </div>
</template>

<script>
export default {
    name: 'Home_Component',

    data() {
        return {
            name: '',
            email: ''
        }
    },
    methods: {
        submit() {
            console.log(this.name, this.email);
        }
    }
}
</script>

<style scoped>

</style>