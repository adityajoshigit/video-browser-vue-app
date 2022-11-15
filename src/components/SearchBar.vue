<template>
    <div id="searchBarCmp">
        <input 
            type="text" 
            name="search-query-tag" 
            id="searchQueryTextBox" 
            placeholder="search query here..."
            @input="onSearchQueryInput" />
    </div>
</template>

<script>
export default {
    name: 'SearchBar',
    methods: {
        onSearchQueryInput(event) {
            this.$emit(
                'searchQueryChange', 
                {
                    searchQuery: event.target.value
                }
            );
        }
    }
}
</script>

<style>

</style>