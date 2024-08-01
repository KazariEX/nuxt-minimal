<script lang="ts" setup>
    declare module "@nuxt/schema" {
        interface PublicRuntimeConfig {}
    }

    const runtimeConfig = useRuntimeConfig();
    const foo: string = runtimeConfig.public.foo;
</script>

<template>
    <span :foo="($route, $router, $config)"></span>
</template>