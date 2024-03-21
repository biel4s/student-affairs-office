<template>
  <h1 class="primary-heading">Edit student</h1>
  <div class="content">
   <p>Test</p>
  </div>
</template>

<script>
definePageMeta({
  layout: 'main',
  data() {
    return {
      students: JSON.parse(sessionStorage.getItem('students')) || []
    }
  },
})
</script>

