<template>
    <DocSectionText v-bind="$attrs">
        <p>Specify the <i>variant</i> property as <i>filled</i> to display the component with a higher visual emphasis than the default <i>outlined</i> style.</p>
    </DocSectionText>
    <div class="card flex justify-center">
        <AutoComplete v-model="value" :suggestions="items" @complete="search" variant="filled" />
    </div>
    <DocSectionCode :code="code" />
</template>

<script setup lang="ts">
import AutoComplete from '@/volt/AutoComplete.vue';
import { ref } from 'vue';

const value = ref(null);
const items = ref([]);

const search = (event) => {
    items.value = [...Array(10).keys()].map((item) => event.query + '-' + item);
};

const code = ref(`
<template>
    <div class="card flex justify-center">
        <AutoComplete v-model="value" :suggestions="items" @complete="search" variant="filled" />
    </div>
</template>

<script setup lang="ts">
import AutoComplete from '@/volt/AutoComplete.vue';
import { ref } from 'vue';

const value = ref(null);
const items = ref([]);

const search = (event) => {
    items.value = [...Array(10).keys()].map((item) => event.query + '-' + item);
}
<\/script>
`);
</script>
