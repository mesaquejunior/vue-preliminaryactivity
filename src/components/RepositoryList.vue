<template>
  <ul>
    <li v-for="(repository, index) in data" :key="index">
      <img
        :src="repository.owner.avatar_url"
        :alt="'Facebook - ' + repository.name"
      />
      <span>
        <strong>{{ repository.name }}</strong>
        <p>
          {{ repository.description }}
        </p>
        <a :href="repository.svn_url" target="_blank">Acesso ao repositório</a>
      </span>
    </li>
  </ul>
</template>

<script>
export default {
  name: 'RepositoryList',
  data() {
    return {
      data: [],
    };
  },
  beforeMount() {
    this.getRepos();
  },
  methods: {
    async getRepos() {
      const res = await fetch('https://api.github.com/orgs/facebook/repos');
      const data = await res.json();
      this.data = data;
    },
  },
};
</script>
