<template>
    <div>
        {{ msg }}
        <br>
        {{ "Name: " + user.name +". Email: " + user.email }}
        <br>
        <button v-on:click="getData" type="button">Get Data</button>
        
    </div>
</template>

<script>
export default {
    name: 'childComponent',
    props: {
        msg: String,
        user: Object,
        getData: Function
    }
    
}
</script>

<style scoped>

</style>