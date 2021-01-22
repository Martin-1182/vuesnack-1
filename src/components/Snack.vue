<template>
    <div class="fixed w-full top-0 left-0 flex justify-center">
        <transition name="snack">
            <div
                v-if="snack"
                class="bg-blue-500 text-white px-8 py-2 rounded-lg text-sm mt-6"
            >
                {{ snack }}
            </div>
        </transition>
    </div>
</template>

<script>
import { mapGetters } from 'vuex'

export default {
    computed: {
        ...mapGetters({
            snack: 'snack/snack'
        })
    }
}
</script>

<style lang="scss" scoped></style>
