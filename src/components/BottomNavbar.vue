<template>
    <div>
        <v-bottom-navigation v-model="value" app>
            <v-btn value="recent" @click="$router.push('/books')">
                <span>Books</span>

                <v-icon>mdi-history</v-icon>
            </v-btn>

            <v-btn value="favorites">
                <span>Authors</span>

                <v-icon>mdi-heart</v-icon>
            </v-btn>

            <v-btn value="nearby">
                <span>Members</span>

                <v-icon>mdi-map-marker</v-icon>
            </v-btn>
        </v-bottom-navigation>
    </div>
</template>

<script>
export default {

}
</script>

<style lang="scss" scoped></style>