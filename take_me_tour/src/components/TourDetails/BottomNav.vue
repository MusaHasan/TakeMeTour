<template>
    <v-container fluid>
        <v-bottom-navigation
            class="hidden-lg-and-up"
            scroll-target="#scroll-area-1"
            hide-on-scroll
            fixed
            horizontal
            >
            <v-btn text color="deep-purple accent-4">
                <span>Recents</span>
                <v-icon>mdi-history</v-icon>
            </v-btn>

            <v-btn text color="deep-purple accent-4">
                <span>Favorites</span>
                <v-icon>mdi-heart</v-icon>
            </v-btn>

            <v-btn text color="deep-purple accent-4">
                <span>Nearby</span>
                <v-icon>mdi-map-marker</v-icon>
            </v-btn>
        </v-bottom-navigation>
    </v-container>
</template>