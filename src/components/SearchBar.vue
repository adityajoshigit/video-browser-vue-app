<template>
    <div id="searchBarCmp">
        <input 
            type="text" 
            name="search-query-tag" 
            id="searchQueryTextBox" 
            placeholder="Some search query goes here..."
            @input="onSearchQueryInput" />
    </div>
</template>

<script>
export default {
    name: 'SearchBar',
    methods: {
        onSearchQueryInput(event) {
            console.log(event.target.value);
        }
    }
}
</script>

<style>

</style>