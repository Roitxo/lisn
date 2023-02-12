<template>
    <nav>
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
        height: 100vh;
        background: rgba(0, 0, 0, 0.2);
        box-shadow: 0 4px 30px rgba(0, 0, 0, 0.1);
        backdrop-filter: blur(13.5px);
        -webkit-backdrop-filter: blur(13.5px);
        border: 1px solid rgba(0, 0, 0, 0.04);
        -webkit-backdrop-filter: blur( 13px );
        padding: 2%;
    }

    li {
        padding: 7% 5%;
        border-bottom: 1px solid #292929;
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