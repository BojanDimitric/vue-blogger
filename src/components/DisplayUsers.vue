<template>
    <div className="container px-0">
        {{}}
    </div>
</template>

<script>

import { fetchUsers } from './services/Userservice';

export default {
    name: 'DisplayUsers',
    data: {
        users: []
    },
    computed: () => {
        users = fetchUsers()
    }
}
</script>

