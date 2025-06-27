<script setup lang="ts">
import DataBsLogo from '../assets/DataBSLogo.svg';
import BackgroundImage from '../assets/image5.png';

interface InputProps {
    showDataBSLogo?: boolean;
}

const props = withDefaults(defineProps<InputProps>(), {
    showDataBSLogo: true,
});
</script>

<template>
    <div class="slidev-layout relative z-2">
        <div class="absolute right-0 right-1 bottom-20 z-0">
            <img :src="BackgroundImage" alt="Background Image" />
        </div>

        <div class="my-auto z-10 relative">
            <slot />
        </div>

        <div v-if="props.showDataBSLogo" class="absolute bottom-10 right-10 z-10">
            <img class="w-15" :src="DataBsLogo" alt="DataBS Logo">
        </div>
    </div>
</template>