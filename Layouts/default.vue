<script setup>

</script>
 
<template>
    <div class="grid grid-cols-1 h-screen grid-rows-[80px_1fr_60px]">
        <LayoutHeader ></LayoutHeader>

        <main >
            <slot />
        </main>

        <LayoutFooter ></LayoutFooter>
    </div>
</template>
 
 
<style scoped></style>