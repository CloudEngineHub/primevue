<template>
    <DocSectionText v-bind="$attrs">
        <p>Label of the tag is defined with the <i>value</i> property.</p>
    </DocSectionText>
    <div class="card flex justify-center">
        <Tag value="New"></Tag>
    </div>
    <DocSectionCode :code="code" />
</template>

<script setup lang="ts">
import Tag from '@/volt/Tag.vue';
import { ref } from 'vue';

const code = ref(`
<template>
    <div class="card flex justify-center">
        <Tag value="New"></Tag>
    </div>
</template>

<script setup lang="ts">
import Tag from '@/volt/Tag.vue';
<\/script>
`);
</script>
