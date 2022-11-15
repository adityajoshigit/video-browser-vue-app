<template>
    <div id="appCmp">
        <SearchBar />
    </div>
</template>

<script>
import SearchBar from './components/SearchBar.vue';
export default {
    name: 'App',
    components: {
        SearchBar: SearchBar
    }
}
</script>