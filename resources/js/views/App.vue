<template>
    <div>
        <header>
            <div class="container">
                <nav class="navbar navbar-expand-lg navbar-light bg-light">
                    <a class="navbar-brand" href="#" id="logo">
                        <img :src="logoImg">
                    </a>
                    <button class="navbar-toggler" type="button" data-toggle="collapse" data-target="#navbarSupportedContent" aria-controls="navbarSupportedContent" aria-expanded="false" aria-label="Toggle navigation">
                        <span class="navbar-toggler-icon"></span>
                    </button>

                    <div class="collapse navbar-collapse" id="navbarSupportedContent">
                        <ul class="navbar-nav mr-auto">
                            <li class="nav-item active">
                                <router-link class="nav-link" :to="{ name: 'home' }">
                                    Home
                                </router-link>
                            </li>
                            <li class="nav-item active">
                                <router-link class="nav-link" :to="{ name: 'contatti' }">
                                    Contatti
                                </router-link>
                            </li>
                        </ul>
                    </div>
                </nav>
            </div>
        </header>
        <main>
            <router-view />
        </main>
    </div>
</template>
<script>
    export default {
        name: "App",
        data() {
            return {
                logoImg: "https://www.boolean.careers/images/misc/logo.png"
            }
        }
    }
</script>
<style scoped>
    #logo img {
        height: 30px;
    }
</style>
