<template>
    <div>
        {{ msg }}
        <br>
        {{ "Name: " + user.name +". Email: " + user.email }}
    </div>
</template>

<script>
export default {
    name: 'childComponent',
    props: {
        msg: String,
        user:Object
    }
    
}
</script>

<style scoped>

</style>