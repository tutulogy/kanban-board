<template>
  <div class="board">
    <div class="row">
        <div class="col-md">
          <progress-lane id="applied" title="Applied" :candidates="applied"></progress-lane>
        </div>
        <div class="col-md">
          <progress-lane id="phone-screening" title="Screening" :candidates="phoneScreenings"></progress-lane>
        </div>
        <div class="col-md">
          <progress-lane id="on-site" title="On Site" :candidates="onSite"></progress-lane>
        </div>
        <div class="col-md">
          <progress-lane id="offer" title="Offer" :candidates="offer"></progress-lane>
        </div>

        <div class="col-md">
          <progress-lane id="rejected" title="Rejected" :candidates="rejected"></progress-lane>
        </div>
    </div>
  </div>
</template>

<script>
import ProgressLane from './ProgressLane'
export default {
  name: 'KanbanBoard',
  components: {
    'progress-lane': ProgressLane
  },
  data () {
    return {
      applied: [
        {
          name: 'Jia'
        },
        {
          name: 'Lydia',
          phone: '123123123'
        }
      ],
      phoneScreenings: [
        {
          name: 'Alex'
        }
      ],
      onSite: [
        {
          name: 'Alex'
        }
      ],
      offer: [
        {
          name: 'Alex'
        }
      ],
      rejected: [
        {
          name: 'Alex'
        }
      ]

    }
  }
}
</script>
