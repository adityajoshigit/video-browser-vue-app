<template>
    <div id="appCmp">
        <SearchBar 
            @searchQueryChange="handleSearchQueryChange"
        />
    </div>
</template>

<script>
import axios from 'axios';
import SearchBar from './components/SearchBar.vue';
const API_KEY = 'AIzaSyAUCwdsA3NrhbcA5g2LUf5JT3nZ5Pk1ZlE';

export default {
    name: 'App',
    components: {
        SearchBar: SearchBar
    },
    methods: {
        handleSearchQueryChange(event) {
            console.log('search term = ', event.searchQuery);
            const searchTerm = event.searchQuery;
            axios.get(
                'https://www.googleapis.com/youtube/v3/search',
                {
                    params: {
                        key: API_KEY,
                        type: 'video',
                        part: 'snippet',
                        q: searchTerm
                    }
                }
            )
            .then(resp => {
                console.log(resp);
            })
        }
    }
}
</script>