<template>
<div>
<h1>Gabe</h1>
<Waiting/>
<Results/>
</div>
</template>

<script>
import Waiting from '../components/Waiting.vue'
import Results from '../components/Results.vue'
export default {
    name: 'home',
  components: {
    Waiting,
    Results
  }
}
</script>

<style>

</style>