<template>
  <div class="home">
    <header>
      <span>Vue.js PWA</span>
    </header>
    <main>
      <aside class="aside">
        <nav class="menu">
          <co-search 
            v-on:search='onSearch'
          ></co-search>
          <co-bookmarks></co-bookmarks>
        </nav>
      </aside>
      <section class="user-app">
        <header class="user-app__header">
          <co-logo></co-logo>
        </header>
        <co-developers></co-developers>
      </section>
    </main>
  </div>
</template>

<script>
import CoSearch from '@/components/CoSearch';
import CoLogo from '@/components/CoLogo';
import CoBookmarks from '@/components/CoBookmarks';
import CoDevelopers from '@/components/CoDevelopers';

export default {
  name: 'Home',
  components: {
    CoSearch,
    CoLogo,
    CoBookmarks,
    CoDevelopers,
  },
  methods: {
    onSearch(searchCriteria) {
      console.log('Search', searchCriteria);
    },
  },
};
</script>
