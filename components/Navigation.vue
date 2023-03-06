<template>
    <nav class="h-screen">
        <div class="logo">
            <h1>.lisn</h1>
        </div>
        <ul>
            <li v-for="(element, index) in menu" :key="index">
                <Icon class="nav-icon" :name="element.icon" size="25px" />
                {{element.name}}
            </li>
        </ul>
    </nav>
</template>

<script>
export default {
    data() {
        return {
            menu: [
                {
                    name: "Inicio",
                    url: "/",
                    icon: "mdi-light:home"
                },
                {
                    name: "Buscar",
                    url: "/search",
                    icon: "mdi-light:magnify"
                },
                {
                    name: "Mi Biblioteca",
                    url: "/library",
                    icon: "mdi-light:music"
                }
            ]
        }
    }
}
</script>

<style scoped>
    nav {
        border: var(--border-color);
        padding: 2%;
        background-color: var(--bg-nav);
    }

    li {
        padding: 7% 5%;
        border-bottom: var(--border-color)
    }

    li:hover {
        background-color: var(--bg);
    }

    .logo {
        font-size: 25px;
        margin: 5%;
    }
    
    .nav-icon {
        margin-right: 20px;
    }
</style>