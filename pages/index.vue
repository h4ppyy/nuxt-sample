<template>
  <div>
    <h1>hello next.js</h1>
    <div>{{ count }}</div>
    <NuxtLink to="/about">
      move about
    </NuxtLink>
    <button @click="plus()">parent plus</button>
    <button @click="minus()">parent minus</button>
    <Sample 
      title="title" 
      :count="count"
      @plus="plus()"
      @minus="minus()"
    />
    <Sample 
      title="title" 
      :count="count"
      @plus="plus()"
      @minus="minus()"
    />
  </div>
</template>

<script>
export default {
  data() {
    return { 
      count: 5 
    }
  },
  methods: {
    plus() {
      this.count = this.count + 1;
    },
    minus() {
      this.count = this.count - 1;
    }
  },
  asyncData() {
    console.log('asyncData')
    return { content: 'Created at: ' + new Date() }
  },
  mounted() {
    console.log('mounted')
  },
  created() {
    console.log('created')
  },
  updated() {
    console.log('updated')
  },
  destroyed() {
    console.log('destroyed')
  },
}
</script>

<style>
</style>
