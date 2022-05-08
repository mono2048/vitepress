<template>
    <h1>
        {{ msg }}
    </h1>
    <h2>{{ count }}</h2>
</template>

<script>
import { ref } from 'vue'
import emitter from "../bus";
export default {
    props:{
        msg: {
            type: String,
            default: ""
        }
    },
    setup () {
        const count = ref(0)
        emitter.on("add",() => count.value++)

        return {
            count
        }
    }
}
</script>

<style lang="scss" scoped>

</style>