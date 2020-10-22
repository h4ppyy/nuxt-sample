<template>
  <div>
    <h1>hello {{ title }} {{ count }}</h1>
    <button @click="$emit('plus')">children plus</button>
    <button @click="$emit('minus')">children minus</button>
  </div>
</template>

<script>
export default {
  props: ['title', 'count'],
  emits: ['plus', 'minus']
}
</script>