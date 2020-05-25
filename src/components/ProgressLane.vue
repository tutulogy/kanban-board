<template>
  <div class="card">
    <h3 class="card-header">{{ title }}</h3>
    <div class="card-body">
      <draggable v-model="draggables" :options="{ group: 'default' }">
        <div v-for="candidate in candidates" :key="candidate.id">
          <item :candidate="candidate"></item>
        </div>
      </draggable>
    </div>
    <div class="card-footer text-muted">{{candidateCount}}</div>
  </div>
</template>

<script>
import Draggable from 'vuedraggable'
import Candidate from './Candidate'
export default {
  name: 'TaskLane',
  props: ['candidates', 'title', 'id'],
  components: {
    item: Candidate,
    draggable: Draggable
  },
  computed: {
    candidateCount () {
      if (!this.candidates) return ''
      if (this.candidates.length === 1) return '1 candidate'
      return `${this.candidates.length} candidates`
    }
  }
}
</script>

<style>
.card-body > * {
  min-height: 50px;
}
</style>
