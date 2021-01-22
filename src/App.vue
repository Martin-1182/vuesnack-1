<template>
    <snack />
    <div class="ml-2 flex">
        <a
            class="bg-blue-900 text-white px-8 py-2 rounded-lg text-xl mt-6"
            href="#"
            @click.prevent="doSomething"
            >Trigger Snack</a
        >
    </div>
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
