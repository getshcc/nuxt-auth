<script setup>
const formData = reactive({
    email: "",
    password: "",
})

const register = async () => {
    try {
        await useFetch("http://localhost:5000/api/users/signup", {
            method: 'POST',
            body: formData
        })
        // return navigateTo('/')
    } catch (error) {
        // errors.value = error
        console.log(error);
    }
}
</script>
 
<template>
    <div class="w-full flex flex-col justify-center items-center pt-32">
        <section>
            <h1 class="text-xl font-bold pb-8">Sign up</h1>
        </section>
        <form @submit.prevent="register" class="flex flex-col gap-4 w-full max-w-[400px]">
            <div class="flex flex-col gap-2">
                <label for="email">Emial:</label>
                <input type="email" id="email" v-model="formData.email"
                    class="p-3 transition-all bg-slate-100 rounded-md ring-offset-2 focus:ring-2 ring-slate-300"
                    autocomplete="off">
            </div>
            <div class="flex flex-col gap-2">
                <label for="password">Password:</label>
                <input type="password" id="password" v-model="formData.password"
                    class="p-3 transition-all bg-slate-100 rounded-md ring-offset-2 focus:ring-2 ring-slate-300">
            </div>
            <div class="w-full flex justify-between items-center">
                <p class="text-xs text-slate-400 leading-5">if you haven't account <br>
                    <NuxtLink to="/login" class="text-slate-900">login</NuxtLink>
                </p>
                <button
                    class="flex items-center justify-between gap-3 bg-green-50 text-green-500 disabled:text-blue-300  hover:bg-green-100 transition-colors font-bold rounded-[6px] p-2 px-5">
                    Sign up
                </button>
            </div>
        </form>
    </div>
</template>
 
 
<style scoped></style>