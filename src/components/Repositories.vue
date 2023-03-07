<!-- <template>
  <div class="container">
    <h1 class="heading">Dzifa's Repositories</h1>
    <div class="list-container">
      <div class="pill" v-for="repo in paginatedRepositories" :key="repo.id">
        <img class="avatar" :src="'https://avatars.dicebear.com/api/big-smile/' + repo.id + '.png'" alt="">
        <router-link :to="{ name: 'Repository', params: { name: repo.name } }">{{ repo.name }}</router-link>
      </div>
    </div>
    <div v-if="pageCount > 1">
      <ul>
        <li v-for="n in pageCount" :key="n">
          <router-link :to="{ name: 'Repositories', query: { page: n } }" @click="updateCurrentPage(n)">{{ n }}</router-link>
        </li>
      </ul>
    </div>
  </div>
</template>

<script type="text/javascript">
export default {
  name: "Repositories",
  data() {
    return {
      repositories: [],
      pagination: {
        perPage: 10,
        currentPage: 1,
      },
    };
  },
  created() {
    this.fetchRepositories();
  },
  methods: {
    fetchRepositories() {
      fetch(`https://api.github.com/users/makydebbie/repos`)
        .then((response) => response.json())
        .then((data) => {
          this.repositories = data;
        });
    },
    updateCurrentPage(page) {
      this.pagination.currentPage = page;
    }
  },
  computed: {
    pageCount() {
      return Math.ceil(this.repositories.length / this.pagination.perPage);
    },
    paginatedRepositories() {
      const startIndex = (this.pagination.currentPage - 1) * this.pagination.perPage;
      const endIndex = startIndex + this.pagination.perPage;
      return this.repositories.slice(startIndex, endIndex);
    },
  },
};
</script>   -->



  
<template>
  <div class="container">
    <h1 class="heading">Dzifa's Repositories</h1>
    <div class="list-container">
      <div class="pill" v-for="repo in paginatedRepositories" :key="repo.id">
        <img class="avatar" :src="'https://avatars.dicebear.com/api/big-smile/' + repo.id + '.png'" alt="">
        <router-link :to="{ name: 'Repository', params: { name: repo.name } }">{{ repo.name }}</router-link>
      </div>
    </div>
    <div v-if="pageCount > 1">
      <ul>
        <li v-for="n in pageCount" :key="n">
          <router-link :to="{ name: 'Repositories', query: { page: n } }" @click="updateCurrentPage(n)">{{ n }}</router-link>
        </li>
      </ul>
    </div>
  </div>
</template>

<!-- Disable eslint rule for component name -->
<!-- eslint-disable vue/multi-word-component-names --> 

<script type="text/javascript">
export default {
  name: "Repositories",
  data() {
    return {
      repositories: [],
      pagination: {
        perPage: 5,
        currentPage: 1,
      },
    };
  },
  created() {
    this.fetchRepositories();
  },
  methods: {
    fetchRepositories() {
      fetch(`https://api.github.com/users/makydebbie/repos`)
        .then((response) => response.json())
        .then((data) => {
          this.repositories = data;
        });
    },
    updateCurrentPage(page) {
      this.pagination.currentPage = page;
    }
  },
  computed: {
    pageCount() {
      return Math.ceil(this.repositories.length / this.pagination.perPage);
    },
    paginatedRepositories() {
      const startIndex = (this.pagination.currentPage - 1) * this.pagination.perPage;
      const endIndex = startIndex + this.pagination.perPage;
      return this.repositories.slice(startIndex, endIndex);
    },
  },
};
</script>