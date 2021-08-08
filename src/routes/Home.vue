<template>
    <Headline/>
    <Search />
    <MovieLists/>
</template>

<script>
import Headline from '~/components/Headline'
import Search from '~/components/Search'
import MovieLists from '~/components/MovieList'

export default {
    components: {
        Headline,
        Search,
        MovieLists
    }
}
</script>
