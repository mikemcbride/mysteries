<template>
  <Layout>
    <h1 class="text-2xl font-semibold mb-8">Prayers of the Rosary</h1>
    <Prayer
      v-for="prayer in prayers"
      :key="prayer.title"
      :title="prayer.title"
      :content="prayer.content" />
  </Layout>
</template>

<script>
import prayers from '@/data/prayers'
import Prayer from '@/components/Prayer'

export default {
  metaInfo: {
    title: 'Prayers of the Rosary'
  },
  components: {
    Prayer,
  },
  data() {
    return {
      prayers: prayers
    }
  }
}
</script>
