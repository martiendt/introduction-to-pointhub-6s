<script setup lang="ts">
import { ref } from 'vue'

const props = defineProps({
  choosen: {
    default: 'usability',
  },
})

const tab = ref(props.choosen)
</script>

<template>
  <div class="text-lg font-medium text-center text-gray-500 border-b border-gray-200 dark:text-gray-400 dark:border-gray-700 font-extrabold">
    <div class="flex flex-wrap -mb-px">
      <span class="mr-2 inline-block p-4 rounded-t-lg border-b-2 border-transparent" :class="{'text-blue-500 border-blue-500': choosen === 'usability'}">
          Usability
      </span>
      <span class="mr-2 inline-block p-4 rounded-t-lg border-b-2 border-transparent" :class="{'text-blue-500 border-blue-500': choosen === 'security'}">
          Security
      </span>
      <span class="mr-2 inline-block p-4 rounded-t-lg border-b-2 border-transparent" :class="{'text-blue-500 border-blue-500': choosen === 'maintainability'}">
          Maintainabilty
      </span>
      <span class="mr-2 inline-block p-4 rounded-t-lg border-b-2 border-transparent" :class="{'text-blue-500 border-blue-500': choosen === 'reliability'}">
          Reliability
      </span>
      <span class="mr-2 inline-block p-4 rounded-t-lg border-b-2 border-transparent" :class="{'text-blue-500 border-blue-500': choosen === 'observability'}">
          Observability
      </span>
      <span class="mr-2 inline-block p-4 rounded-t-lg border-b-2 border-transparent" :class="{'text-blue-500 border-blue-500': choosen === 'scalability'}">
          Scalability
      </span>
    </div>
  </div>
</template>
