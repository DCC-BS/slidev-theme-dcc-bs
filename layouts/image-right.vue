<script lang="ts" setup>
import DataBsLogo from '../assets/DataBSLogo.svg';
import BackgroundImage from '../assets/image5.png';

interface InputProps {
    image: string;
}

const props = defineProps<InputProps>();

</script>

<template>
    <div class="slidev-layout relative">
        <div class="flex justify-stretch gap-2 z-5">
            <div>
                <slot />
            </div>
            <div>
                <img :src="props.image" alt="Right Image" class="w-full h-auto object-cover" />
            </div>
        </div>

        <div class="absolute right-0 right-1 bottom-20 z-0">
            <img :src="BackgroundImage" alt="Background Image" />
        </div>
        <div class="absolute bottom-10 right-10 z-10">
            <img class="w-15" :src="DataBsLogo" alt="DataBS Logo">
        </div>
    </div>
</template>