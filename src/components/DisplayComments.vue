<template>
    <div className="container px-0">
        {{}}
    </div>
</template>

<script>

import { fetchComments } from './services/Commentservice';

export default {
    name: 'DisplayComments',
    data: {
        users: []
    },
    computed: () => {
        users = fetchComments();
    }
}
</script>

