<template>
    <div className="container px-0">
        {{}}
    </div>
</template>

<script>

import { fetchPosts } from './services/Postservice';

export default {
    name: 'DisplayPosts',
    data: {
        posts: []
    },
    computed: () => {
        posts = fetchPosts();
    }
}
</script>

