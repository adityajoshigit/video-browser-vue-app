<template>
    <div id="appCmp">
        <SearchBar 
            @searchQueryChange="handleSearchQueryChange"
        />
    </div>
</template>

<script>
import SearchBar from './components/SearchBar.vue';
export default {
    name: 'App',
    components: {
        SearchBar: SearchBar
    },
    methods: {
        handleSearchQueryChange(event) {
            console.log('search term = ', event.searchQuery);
        }
    }
}
</script>