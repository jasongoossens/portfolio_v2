<template>
    <img alt="Vue logo" src="./assets/logo.png" />
    <HelloWorld msg="Welcome to Your Vue.js App" />
    <div
        v-for="(project, index) in projects.items"
        :key="index"
        class="project"
    >
        <h1>{{ project.name }}</h1>
        <ul>
            <li
                v-for="(technology, index) in project.technologies"
                :key="index"
            >
                {{ technology.name }}
            </li>
        </ul>
    </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue';
import projects from './data/projects';

export default {
    name: 'App',
    components: {
        HelloWorld,
    },
    data() {
        return { projects };
    },
};
console.log(projects);
</script>

<style lang="scss">
#app {
    font-family: Avenir, Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    text-align: center;
    color: #2c3e50;
    margin-top: 60px;
}
</style>
