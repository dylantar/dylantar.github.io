<template>
    <PrimePanel header="My Resume" class="my-6">
      <ul>
        <li><strong>Education:</strong> B.S. in Computer Science, XYZ University</li>
        <li><strong>Skills:</strong> HTML, CSS, JavaScript, Vue.js, Node.js</li>
        <li><strong>Experience:</strong> Web Developer Intern at ABC Company</li>
      </ul>
      <PrimeButton label="Download Resume" icon="pi pi-download" :href="'/path/to/resume.pdf'" />
    </PrimePanel>
  </template>
  
  <script setup>
  </script>
  
  <style scoped>
  /* Add any additional styles if needed */
  </style>
  