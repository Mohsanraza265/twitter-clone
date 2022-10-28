<template>
    <div>
       <SidebarMainSection title="Home" :loading="loading">
           this is home page...
       </SidebarMainSection>

    </div>
</template>

<script setup>
const loading = ref(false)
</script>