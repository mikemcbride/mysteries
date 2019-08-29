<template>
  <Layout>
    <h1 class="text-2xl font-semibold mb-4">Mysteries of the Rosary</h1>
    <p v-if="suggested !== null" class="mb-8">Suggested mysteries for today are the <span class="font-bold">{{ suggested }}</span></p>
    <Mystery
      v-for="mystery in mysteries"
      :key="mystery.name"
      :name="mystery.name"
      :days="mystery.days"
      :mysteries="mystery.mysteries" />
  </Layout>
</template>

<script>
import mysteries from '@/data/mysteries'
import Mystery from '@/components/Mystery'

export default {
  metaInfo: {
    title: 'Mysteries of the Rosary'
  },
  components: {
    Mystery,
  },
  data() {
    return {
      mysteries: mysteries,
      suggested: null
    }
  },
  created() {
    switch (new Date().getDay()) {
      case 0:
      case 3:
        this.suggested = 'Glorious'
        break
      case 1:
      case 6:
        this.suggested = 'Joyful'
        break
      case 2:
      case 5:
        this.suggested = 'Sorrowful'
        break;
      case 4:
        this.suggested = 'Luminous'
        break
      default:
        this.suggested = null
    }
  },
}
</script>
