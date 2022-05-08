<template>
    <div>
        <button @click="onClick">add</button>
    </div>
</template>

<script>
import emitter from "../bus";
export default {
    setup () {
        const onClick = () => {
            emitter.emit("add")
        }

        return {onClick}
    }
}
</script>

<style lang="scss" scoped>

</style>