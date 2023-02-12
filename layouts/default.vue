<template>
    <div class="main flex dark">
        <div class="navbar w-2/12">
            <Navigation />
        </div>
        <div class="w-10/12">
            <Topbar />
            <NuxtPage class="content"/>
        </div>
    </div>
</template>

<style>
    :root {
        --primary: #FF6E31;
    }

    .dark {
        --bg-nav: #1b1a1b;
        --bg: #151515;
        --color: white;
    }

    .main {
        background-color: var(--bg);
        color: var(--color);
    }

    .content {
        padding: 2.5%;
    }
</style>