<template>
    <div className="container px-0">
        {{}}
    </div>
</template>

<script>

import { fetchBlogs } from './services/Blogservice';

export default {
    name: 'DisplayBlogs',
    data: {
        users: []
    },
    computed: () => {
        users = fetchBlogs();
    }
}
</script>

