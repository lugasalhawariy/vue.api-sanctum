<template>
    <div class="login container mt-3">
        <div class="row">
            <div class="col-12 col-md-6">
                <div class="card">
                    <div class="card-header">Login Page</div>
                    <div class="card-body">
                        <form action="POST" @submit.prevent="login">
                            <div class="form-group mt-2">
                                <label for="email">Email</label>
                                <input v-model="form.email" type="text" id="email" class="form-control">
                            </div>
                            <div class="form-group mt-2 mb-3">
                                <label for="password">Password</label>
                                <input v-model="form.password" type="password" id="password" class="form-control">
                            </div>
                            <button type="submit" class="btn btn-primary w-100">Login</button>
                        </form>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
import axios from 'axios';
axios.defaults.withCredentials = true;

export default {
    data () {
        return {
            form: {
                email: '',
                password: ''
            },
        }
    },
    methods: {
        async login() {
            await axios.get("http://localhost/sanctum/csrf-cookie");
            await axios.post("http://localhost/login", this.form);
            let user = await axios.get('http://localhost/user');
            console.log(user.data);
        },
    }
}
</script>

<style>

</style>