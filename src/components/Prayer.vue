<template functional>
  <div>
    <h2 class="text-xl font-medium mb-2">{{ props.title }}</h2>
    <p class="mb-8 leading-loose">{{ props.content }}</p>
  </div>
</template>

<script>
export default {
  name: 'Prayer',
  props: {
    title: {
      type: String,
      required: true
    },
    content: {
      type: String,
      required: true
    }
  }
}
</script>
