<template>
  <div class="card task-lane-item">
    <div class="card-block">
        <h5 class="card-title">
            Name: {{candidate.name}}
            Phone: {{candidate.phone}}
        </h5>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Candidate',
  props: ['candidate']
}
</script>

<style>
.card.task-lane-item {
  background:rgb(91, 91, 114);
}
</style>
