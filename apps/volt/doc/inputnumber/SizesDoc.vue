<template>
    <DocSectionText v-bind="$attrs">
        <p>InputNumber provides <i>small</i> and <i>large</i> sizes as alternatives to the base.</p>
    </DocSectionText>
    <div class="card flex flex-col items-center gap-4">
        <InputNumber v-model="value1" size="small" placeholder="Small" mode="currency" currency="USD" locale="en-US" />
        <InputNumber v-model="value2" placeholder="Normal" mode="currency" currency="USD" locale="en-US" />
        <InputNumber v-model="value3" size="large" placeholder="Large" mode="currency" currency="USD" locale="en-US" />
    </div>
    <DocSectionCode :code="code" />
</template>

<script setup lang="ts">
import InputNumber from '@/volt/InputNumber.vue';
import { ref } from 'vue';

const value1 = ref(null);
const value2 = ref(null);
const value3 = ref(null);

const code = ref(`
<template>
    <div class="card flex flex-col items-center gap-4">
        <InputNumber v-model="value1" size="small" placeholder="Small" mode="currency" currency="USD" locale="en-US" />
        <InputNumber v-model="value2" placeholder="Normal" mode="currency" currency="USD" locale="en-US" />
        <InputNumber v-model="value3" size="large" placeholder="Large" mode="currency" currency="USD" locale="en-US" />
    </div>
</template>

<script setup lang="ts">
import InputNumber from '@/volt/InputNumber.vue';
import { ref } from 'vue';

const value1 = ref(null);
const value2 = ref(null);
const value3 = ref(null);
<\/script>
`);
</script>
