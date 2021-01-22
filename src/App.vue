<template>
    <snack />
    <a href="#" @click.prevent="doSomething">Trigger Snack</a>
</template>
<script>
import { mapActions } from 'vuex'
import Snack from '@/components/Snack'
export default {
    name: 'App',

    components: {
        Snack
    },
    methods: {
        ...mapActions({
            snack: 'snack/snack'
        }),

        doSomething() {
            this.snack('This is a snack!')
        }
    }
}
</script>

<style src="./assets/styles/app.css"></style>
