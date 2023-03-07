<template>
    <div>
      <h1>{{ repository.name }}</h1>
      <p>{{ repository.description }}</p>
      <p>Stars: {{ repository.stargazers_count }}</p>
      <p>Forks: {{ repository.forks_count }}</p>
    </div>
  </template>
  
<!-- Disable eslint rule for component name -->
<!-- eslint-disable vue/multi-word-component-names -->
  <script type="text/javascript">
  export default {
    name: "Repository",
    data() {
      return {
        repository: {}
      }
    },
    created() {
  const repositoryName = this.$route.params.name;
  fetch(`https://api.github.com/repos/makydebbie/${repositoryName}`)
    .then(response => response.json())
    .then(data => {
      this.repository = data;
    });
    }
  }
  </script>