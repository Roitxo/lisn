<template>
    <div class="topbar flex items-center">
        <div class="options w-8/12">
            <div class="page-title flex items-center">
                <span>{{greeting}}, Juanes Roig</span>
            </div>
        </div>
        <div class="options flex items-center justify-end w-4/12">
            <div class="color-mode-switch flex items-center">
                <button class="color-mode-switch">
                    <Icon @click="colorMode.preference = 'light'" v-if="colorMode.preference == 'dark'"
                        name="ph:moon-bold" size="23px" />
                    <Icon @click="colorMode.preference = 'dark'" v-if="colorMode.preference == 'light'"
                        name="ph:sun-bold" size="23px" />
                </button>
            </div>
            <div class="avatar flex items-center">
                <Icon name="mdi-light:account" size="30px" />
                <span>Juanes Roig</span>
            </div>
        </div>
    </div>
</template>

<script setup>
import moment from 'moment';
moment().format();

const colorMode = useColorMode()
const greeting = moment().isAfter(moment().format(`YYYY-MM-DD 20:00:00`)) ? "Buenas noches"
    : moment().isAfter(moment().format(`YYYY-MM-DD 13:00:00`)) ? "Buenas tardes"
        : moment().isAfter(moment().format(`YYYY-MM-DD 05:00:00`)) ? "Buenos días"
            : "Buenas noches"

</script>

<style scoped>
.topbar {
    padding: 1.5%;
    border-bottom: var(--border-color);
}

.page-title {
    font-size: 25px;
}

.options div {
    margin: 0 2%;
}
</style>