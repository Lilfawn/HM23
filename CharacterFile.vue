<template>
  <li class="list-group-item">
    <div class="d-inline-block me-3">{{ character.title }}</div>
    <div class="btn-group btn-group-sm" role="group" aria-label="Basic example">
      <button type="button" class="btn btn-outline-primary" @click="decreaseCount">-</button>
      <button type="button" class="btn btn-primary">{{ character.count }}</button>
      <button type="button" class="btn btn-outline-primary" @click="increaseCount">+</button>
    </div>
  </li>
</template>

<script>
export default {
  props: {
    character: Object
  },
  methods: {
    increaseCount() {
      this.character.count++;
    },
    decreaseCount() {
      if (this.character.count > 0) {
        this.character.count--;
      }
    }
  }
}
</script>