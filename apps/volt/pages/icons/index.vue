<template>
    <div>
        <Head>
            <Title>Icons - Volt</Title>
            <Meta name="description" content="Volt components can be used with any icon library using the templating features." />
        </Head>

        <div class="doc">
            <div class="doc-main">
                <div class="doc-intro">
                    <h1>Icons</h1>
                    <p>Volt components can be used with any icon library using the templating features.</p>
                </div>
                <DocSections :docs="docs" />
            </div>
            <DocSectionNav :docs="docs" />
        </div>
    </div>
</template>

<script setup lang="ts">
import FontAwesomeDoc from '@/doc/icons/FontAwesomeDoc.vue';
import ImageDoc from '@/doc/icons/ImageDoc.vue';
import MaterialDoc from '@/doc/icons/MaterialDoc.vue';
import PrimeIconsDoc from '@/doc/icons/PrimeIconsDoc.vue';
import SVGDoc from '@/doc/icons/SVGDoc.vue';
import { ref } from 'vue';

const docs = ref([
    {
        id: 'primeicons',
        label: 'PrimeIcons',
        component: PrimeIconsDoc
    },
    {
        id: 'material',
        label: 'Material',
        component: MaterialDoc
    },
    {
        id: 'fontawesome',
        label: 'FontAwesome',
        component: FontAwesomeDoc
    },
    {
        id: 'svg',
        label: 'SVG',
        component: SVGDoc
    },
    {
        id: 'image',
        label: 'Image',
        component: ImageDoc
    }
]);
</script>
