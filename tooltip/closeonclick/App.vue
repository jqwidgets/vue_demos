<template>
    <div id="container">
        <JqxTooltip :theme="'material'" 
            :autoHide="false" :position="'bottom'" :name="'movieTooltip'"
            :content="'The Amazing Spider-Man'">
            <img src='https://www.jqwidgets.com/vue/images/The_Amazng_Spider_Man.jpeg' />
        </JqxTooltip>
        <JqxTooltip :theme="'material'" 
            :autoHide="false" :position="'bottom'" :name="'movieTooltip'"
            :content="'The Avengers'">
            <img src='https://www.jqwidgets.com/vue/images/The_Avengers.jpg' />
        </JqxTooltip>
        <JqxTooltip :theme="'material'" 
            :autoHide="false" :position="'bottom'" :name="'movieTooltip'"
            :content="'The Dark Knight Rise'">
            <img src='https://www.jqwidgets.com/vue/images/The_Dark_Knight_Rises.jpg' />
        </JqxTooltip>
    </div>
</template>

<script>
    import JqxTooltip from 'jqwidgets-scripts/jqwidgets-vue/vue_jqxtooltip.vue';

    export default {
        components: {
            JqxTooltip
        }
    }
</script>

<style>
  
    #container {
        width: 400px;   
        margin-left: 200px;
    }
    #container div {
        margin: 8px 8px 0 8px;
        float: left;
    }
  
</style>