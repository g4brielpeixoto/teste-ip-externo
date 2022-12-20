<script>

export default {
  created() {
    fetch('https://api.ipify.org?format=json')
      .then(response => response.json())
      .then(data => this.ip = data.ip)
  },
  data() {
    return {
      ip: 'Hello Vue!'
    }
  },
}
</script>

<template>
  <div>
    {{ ip }}
  </div>
</template>

