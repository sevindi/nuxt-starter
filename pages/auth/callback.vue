<template>
    <div class="text-center">
        <n-result v-if="$route.query.error" status="error" title="Failed to login"
            :description="$route.query.error.toString()">
            <template #footer>
                <NuxtLink to="/auth/login" class="no-underline">
                    <n-button type="primary">Go back to login</n-button>
                </NuxtLink>
            </template>
        </n-result>

        <n-spin v-else size="large"></n-spin>
    </div>
</template>

<script setup>
definePageMeta({
    auth: false,
    colorMode: "light",
    layout: "auth"
})
</script>