<template>
    <header>
        <!-- Navbar -->
        <nav class="navbar navbar-expand-lg navbar-light bg-white">
            <div class="container-fluid">
                <button class="navbar-toggler" type="button" data-mdb-toggle="collapse" data-mdb-target="#navbarExample01"
                    aria-controls="navbarExample01" aria-expanded="false" aria-label="Toggle navigation">
                    <i class="fas fa-bars"></i>
                </button>
                <div class="collapse navbar-collapse" id="navbarExample01">
                    <ul class="navbar-nav me-auto mb-2 mb-lg-0">
                        <li class="nav-item active" @click="goHome">
                            <p class="nav-link">Home</p>
                        </li>
                        <li class="nav-item" @click="goLogin">
                            <p class="nav-link">Login</p>
                        </li>
                        <!-- <li class="nav-item">
                            <a class="nav-link" href="#">Pricing</a>
                        </li> -->
                        <li class="nav-item">
                            <a class="nav-link" href="https://amzlucas.github.io/Dotu-CV/" target="_blank">About</a>
                        </li>
                    </ul>
                </div>
            </div>
        </nav>
        <!-- Navbar -->

        <!-- Jumbotron -->
        <div class="p-2 text-center bg-light">
            <h1 class="mb-3">To-do list</h1>
            <!-- <h4 class="mb-3">Subheading</h4>
            <a class="btn btn-primary" href="" role="button">Call to action</a> -->
        </div>
        <!-- Jumbotron -->
    </header>
</template>
<script>
export default {
    name: 'Header',
    methods: {
        goHome: function () {
            this.$router.push({ path: '/' })
        },
        goLogin: function () {
            this.$router.push({ path: './login' })
        }
    }
}
</script>
<style scoped>
.nav-link {
    cursor: pointer;
}
</style>