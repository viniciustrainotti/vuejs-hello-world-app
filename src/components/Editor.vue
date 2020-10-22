<template>
    <div>
        <h1>Editor</h1>
        <textarea v-model="content2">
        </textarea>
        <h2>Preview</h2>
        <div v-preview="content2" class="preview"></div>
        <code>
            Even if you forget to close the tag, 
            it does not affect the outside
        </code>
    </div>
</template>

<script>
export default {
    name: 'Editor',
    data: function() {
        return {
            content2: '<b>test</b>',
        }
    }    
}
</script>

<style scoped>

</style>