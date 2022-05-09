<template>
    <div class="p-3 px-40 flex border-b-2">
        <nuxt-link to="/"  class="logo left-side mr-auto py-1 text-3xl font-semibold">
            U Platform
        </nuxt-link>
        <div class="right-side ml-auto flex space-x-4 text-lg">
            <nuxt-link to="/signup" class="registration font-medium hover:border-red-700 border-transparent border-b-2 cursor-pointer py-2 px-3 cursor-pointer">Sign Up</nuxt-link>
            <nuxt-link to="/login" class="login font-medium hover:border-red-700 border-transparent border-b-2
 cursor-pointer py-2 px-3 cursor-pointer">Login</nuxt-link>
        </div>
    </div>
</template>

<script>
export default {
    methods:{
    }
}
</script>