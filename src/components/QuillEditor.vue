<template>
  <div>
    <vue-editor v-model="content"></vue-editor>
    <div v-html="content"></div>
    <button v-on:click="testando()">SALVAR</button>
  </div>
</template>

<script>
import { VueEditor } from "vue2-editor";

export default {
    name: 'VueTestEditor',
    components: {
        VueEditor
    },
    watch: {
        content: function(){
            console.log(this.content);
        }
    },
    data() {
        return {
            content: "<img src='https://static.pexels.com/photos/177809/pexels-photo-177809.jpeg'>"
        };
    },
    methods:{
        testando: function (){
            console.log('SALVANDO O TEXTO', this.content);
        }
    }
};
</script>