<template>
    <div>
        <app-header title="Books"></app-header>
        <template>
            <v-card class="mx-auto" tile>
                <v-list dense>
                    <v-list-item v-for="(item, i) in books" :key="i">
                        <v-list-item-avatar>
                            <v-img :src="item.img"></v-img>
                        </v-list-item-avatar>

                        <v-list-item-content>
                            <v-list-item-title>{{ item.title }}</v-list-item-title>
                            <v-list-item-subtitle>{{ item.author.name }}</v-list-item-subtitle>
                            <v-list-item-subtitle>Pages : {{ item.pages }}</v-list-item-subtitle>
                        </v-list-item-content>

                        <v-list-item-icon>
                            <div>
                                <v-menu offset-y>
                                    <template v-slot:activator="{ on, attrs }">
                                        <v-btn v-bind="attrs" v-on="on" text>
                                            <v-icon>mdi-dots-vertical</v-icon>
                                        </v-btn>
                                    </template>
                                    <v-list>
                                        <v-list-item>
                                            <v-list-item-title>Edit</v-list-item-title>
                                            <v-icon>mdi-pencil</v-icon>
                                        </v-list-item>
                                        <v-list-item>
                                            <v-list-item-title>Delete</v-list-item-title>
                                            <v-icon>mdi-delete</v-icon>
                                        </v-list-item>
                                        <v-list-item>
                                            <v-list-item-title>Return</v-list-item-title>
                                        </v-list-item>
                                        <v-list-item>
                                            <v-list-item-title>Issue</v-list-item-title>
                                        </v-list-item>
                                    </v-list>
                                </v-menu>
                                <p>Status</p>
                            </div>
                        </v-list-item-icon>
                    </v-list-item>
                </v-list>
            </v-card>
        </template>
    </div>
</template>

<script>
import booksList from "@/data/books.json";
import AppHeader from '@/components/AppHeader.vue';
export default {
    components: { AppHeader },
    data() {
        return {
            books: booksList
        }
    }
}
</script>

<style lang="scss" scoped></style>