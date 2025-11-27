<template>
    <button @click="count++" class="btn btn-primary">You clicked me {{ count }} times.</button>
</template>
<script>
    import { ref } from 'vue';
    export default{
        setup(){
            const count = ref(0);

            return {
                count
            }
        }
    }
</script>