<template>
    <div class="main flex" :class="`${colorMode.preference}-mode`">
        <div class="navbar w-2/12">
            <Navigation />
        </div>
        <div class="w-10/12">
            <Topbar />
            <NuxtPage class="content"/>
            <FixedPlayer />
        </div>
    </div>
</template>

<script setup>
    const colorMode = useColorMode()
    colorMode.preference = "dark"
</script>

<style>
    /**Importar fuentes */
    @import url('https://fonts.googleapis.com/css2?family=Poppins:wght@100;200;300;400;500;600;700;800;900&display=swap');

    :root {
        --primary: #FF6E31;
    }

    .dark-mode {
        --bg-nav: #0e1629;
        --bg: #1A1A2E;
        --color: white;
        --low-color: rgb(163, 160, 160);
        --border-color: .5px solid rgba(255, 255, 255, 0.048);
    }

    .light-mode {
        --bg-nav: #E1E5EA;
        --bg: #FAF3F3;
        --color: rgb(17, 16, 16);
        --low-color: rgb(56, 56, 56);
        --border-color: .5px solid rgba(5, 5, 5, 0.144);
    }

    .main {
        background-color: var(--bg);
        color: var(--color);
        font-family: 'Poppins', sans-serif;
    }

    .content {
        padding: 2.5%;
    }
</style>