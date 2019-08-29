<template functional>
  <div>
    <h2 class="text-xl font-medium mb-2">The {{ props.name }} Mysteries</h2>
    <p class="mb-4 text-gray-700">Suggested on {{ props.days }}</p>
    <ol class="mb-8 list-decimal pl-6 leading-loose">
      <li v-for="(mystery, $index) in props.mysteries" :key="$index">{{ mystery }}</li>
    </ol>
  </div>
</template>

<script>
export default {
  name: 'Mystery',
  props: {
    name: {
      type: String,
      required: true
    },
    days: {
      type: String, 
      required: true
    },
    mysteries: {
      type: Array,
      required: true
    }
  }
}
</script>
