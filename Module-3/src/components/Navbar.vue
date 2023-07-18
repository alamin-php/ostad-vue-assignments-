<script setup>
    import MenuItem from './MenuItem.vue';
</script>

<template>
    <nav class="site-nav dark js-site-navbar mb-5 site-navbar-target">
        <div class="container">
            <div class="site-navigation">
                <a href="#" class="logo m-0 float-left">Launch<span class="text-primary">.</span></a>

                <MenuItem />

                <ul class="js-clone-nav d-none mt-1 d-lg-inline-block site-menu float-right">
                    <li class="cta-button-outline"><a href="#">Sign in</a></li>
                    <li class="cta-primary"><a href="#">Register</a></li>
                </ul>

                <a href="#" class="burger ml-auto float-right site-menu-toggle js-menu-toggle d-inline-block dark d-lg-none" data-toggle="collapse" data-target="#main-navbar">
                <span></span>
                </a>
            </div>
        </div>
    </nav>
</template>

<style scoped>
</style>