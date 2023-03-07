<template>
    <div class="fixed-player flex items-center fixed bottom-0 w-screen">
        <img class="w-16 h-16" src="https://www.lahiguera.net/musicalia/artistas/maneskin/disco/12592/maneskin_rush-portada.jpg" alt="player-thumbnail">
        <div class="song-info mx-5">
            <div class="song">DON'T WANNA SLEEP</div>
            <div class="artist">Maneskin</div>
        </div>
        <div class="flex items-center song-control">
            <Icon name="tabler:player-skip-back" />
            <Icon class="mx-3" name="tabler:player-play" size="30px" />
            <Icon name="tabler:player-skip-forward" />
            <input class="mx-5 control-slider" type="range" max="100" min="0">
            <Icon name="material-symbols:volume-up-outline-rounded" size="20px" />
            <input class="mx-5" type="range" max="100" min="0">
        </div>
    </div>
</template>

<style scoped>
    .fixed-player {
        padding: 1% 2%;
        border-top: var(--border-color);
    }

    .artist {
        color: var(--low-color);
    }

    .control-slider {
        width: 40vw;
    }
</style>