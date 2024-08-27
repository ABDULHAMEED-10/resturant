<template>
    <div>

        <input type="text" placeholder="name" v-model="name">
        <br />
        <br />
        <input type="text" placeholder="email" v-model="email">
        <br />
        <br />
        <button v-on:click="submit" type="button">Submit</button>

        <br />
        <label for="java">Java</label>
        <input type="checkbox" id="java" value="java" v-model="checkedNames">
        <label for="python">Python</label>
        <input type="checkbox" id="python" value="python" v-model="checkedNames">
        <label for="php">PHP</label>
        <input type="checkbox" id="php" value="php" v-model="checkedNames">
        <br>
        <span>Checked Language: {{ checkedNames }}</span>
        <br>

        <label for="teacher">Teacher</label>
        <input type="radio" name="profession" value="Teacher" v-model="who" id="teacher">
        <label for="student">Student</label>
        <input type="radio" name="profession" value="student" v-model="who" id="student">
        <br>
        <span>I am: {{who}}</span>
        <br>
        <br>
        <h1 v-if="show">if condition</h1>
        <h1 v-else>else condition</h1>
        <button v-on:click="show = !show" type="button">Toggle</button>
        <br>
        <br>
        <ul>
            <h4>Checked Languages are</h4>
            <li v-for="name in checkedNames" :key="name">{{ name }} </li>
        </ul>

        <br>
        <br>
        <childComponent :msg=who :user=user :getData="submit" />
    </div>
</template>

<script>
import childComponent from './Child.vue';

export default {
    name: 'Home_Component',
    components: {
        childComponent
    },
    data() {
        return {
            name: '',
            email: '',
            checkedNames: [],
            who: '',
            show: true,
            user: {
                name: 'John Doe',
                email: 'john@gmail.com'
            }
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
