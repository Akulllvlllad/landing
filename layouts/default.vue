<template>
    <naive-config>
        <Header />
      <slot />
    </naive-config>
</template>

<script>
import Header from '~/components/header.vue'
export default {
    components: {
        Header
    }
}

</script>