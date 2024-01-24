<script setup></script>

<template>
    <div>
        <header class="w-full h-full flex justify-between items-center">
            <div class="flex items-center">
                <h1 class="font-bold text-lg p-2">Auth</h1>
                <nav class="flex">
                    <NuxtLink active-class="font-medium border-b border-black" class="p-2" to="/">Home</NuxtLink>
                </nav>
            </div>
            <div>
                <nav class="flex gap-2">
                    <div class="flex gap-3">
                        <NuxtLink active-class="font-medium border-b border-black" class="p-2" to="/login">Login</NuxtLink>
                        <NuxtLink active-class="font-medium border-b border-black" class="p-2" to="/sign-up">Sign up
                        </NuxtLink>
                    </div>
                </nav>
            </div>
        </header>
    </div>
</template>