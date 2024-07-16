<script setup>
import { ref, computed, onMounted, onBeforeUnmount } from 'vue';
import { useLayout } from '@/layout/composables/layout';
import { useRouter } from 'vue-router';

const { layoutConfig, onMenuToggle } = useLayout();


const router = useRouter();

const logoUrl = computed(() => {
    return `/layout/images/${layoutConfig.darkTheme.value ? 'gears.png' : 'gears.png'}`;
});


</script>


<template>
    <div className="card align-items-center">
        <h2>Em construção...</h2>
        <!-- <p>Use this page to start from scratch and place your custom content.</p> -->
        <img :src="logoUrl" alt="logo" />
        <!-- <span>eLegis</span> -->
    </div>
</template>