<template>
    <div>
        <nav class="navbar navbar-expand-lg navbar-light bg-light">
            <div class="container">
                <a class="navbar-brand" href="#">Vue Sanctum</a>
                <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNav" aria-controls="navbarNav" aria-expanded="false" aria-label="Toggle navigation">
                <span class="navbar-toggler-icon"></span>
                </button>
                <div class="collapse navbar-collapse" id="navbarNav">
                <ul class="navbar-nav">
                    <li class="nav-item">
                    <router-link class="nav-link" exact to="/">Home</router-link>
                    </li>
                    <li class="nav-item">
                    <router-link class="nav-link" to="/user">User</router-link>
                    </li>
                    <li class="nav-item">
                    <router-link class="nav-link" to="/login">Login</router-link>
                    </li>
                </ul>
                </div>
            </div>
        </nav>
    </div>
</template>
