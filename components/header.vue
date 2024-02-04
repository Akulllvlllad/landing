

<template>
    <header>
        <NPageHeader ref="header">
            <template #title>
                <NIcon @click="active = true" size="40">
                    <Dots />
                </NIcon>
            </template>
            
            <template #extra>
                <n-avatar
                    object-fit="cover"
                    src="https://gazeta.sfu-kras.ru/files/gazeta/Bogdanova.jpg"
                />
            </template>
        
        </NPageHeader>
    </header>

    <NDrawer v-model:show="active" width="80%" placement="left">
        <NDrawerContent title="Меню">
        
        </NDrawerContent>
    </NDrawer>
</template>

<script>
import { Dots } from '@vicons/tabler'

export default {
    mounted(){
        

        window.addEventListener('scroll', () => window)
    },
    data(){
        return {
            active: false,
        }
    },

    components: {
        Dots
    },
}


</script>


