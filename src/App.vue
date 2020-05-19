<template>
    <div id="app">
        <b-container class="section">
            <div class="fixed-top">
                <b-container class="title-header-container">
                    <h1 class="title-header">Lake Beulah</h1>
                </b-container>
            </div>
            <b-container role="tablist" class="fixed-top actions-tablist">
                <b-collapse
                    v-bind:class="{ hidden: isHidden }"
                    class="action-card"
                    id="sailing"
                    accordion="accordian1"
                >
                    <b-card>
                        <SailingTemplate></SailingTemplate>
                    </b-card>
                </b-collapse>
                <b-collapse id="history" accordion="accordian1">
                    <b-card>history section!</b-card>
                </b-collapse>
                <b-collapse id="realEstate" accordion="accordian1">
                    <b-card>realestate section!</b-card>
                </b-collapse>
            </b-container>
        </b-container>
        <Actions></Actions>
    </div>
</template>

<script>
import Vue from "vue";
import { BootstrapVue, IconsPlugin } from "bootstrap-vue";
import Actions from "./components/Actions";
import SailingTemplate from "./components/SailingTemplate";

// Install BootstrapVue
Vue.use(BootstrapVue);
// Optionally install the BootstrapVue icon components plugin
Vue.use(IconsPlugin);
import "bootstrap/dist/css/bootstrap.css";
import "bootstrap-vue/dist/bootstrap-vue.css";

export default {
    name: "App",
    components: {
        Actions,
        SailingTemplate,
    },
};
</script>

<style scoped>
#app {
    font-family: Avenir, Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    text-align: center;
    color: #2c3e50;
    margin-top: -20rem;
    max-width: 60rem;
    margin-left: auto;
    margin-right: auto;
    display: flex;
    flex-direction: column;
}

.actions-tablist {
    display: flex;
    margin-top: 6rem;
    justify-content: center;
    align-items: center;
    position: fixed;
}

.hidden {
    display: none;
}

.title-header-container {
    order: 1;
    width: 50%;
    height: 9vw;
    margin-top: 2rem;
    position: sticky;
    background: rgba(66, 66, 66, 1);
    border-radius: 20px;
}

.title-header {
    color: white;
    font-size: 5vw;
    line-height: 50px;
    font-weight: 100;
    letter-spacing: 1px;
    margin: 0;
    position: absolute;
    top: 50%;
    left: 50%;
    margin-right: -50%;
    transform: translate(-50%, -50%);
}

.video-container {
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
}

.outer-wrapper {
    margin-top: 1rem;
}

.section {
    position: relative;
    width: 100%;
    height: 120vh;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    align-content: flex-start;
    overflow: hidden;
    margin-bottom: 2rem;
    flex-wrap: nowrap;
}
</style>
