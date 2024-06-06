<template>
    <div>
        <h1>Welcome to PT GIT Solution</h1>
        <p>Solusi Teknologi Terbaik untuk Bisnis Anda</p>
    </div>
</template>

<script>
import axios from 'axios';
export default {
    name: 'Home',
    data() {
        return {
            profile: {}
        };
    },
    created() {
        axios.get('http://localhost:3000/profile')
            .then(response => {
                this.profile = response.data;
            })
            .catch(error => {
                console.log(error);
            });
    }
};
</script>