<template>
  <v-navigation-drawer expand-on-hover rail>
    <v-list>
        <v-list-item prepend-avatar="https://randomuser.me/api/portraits/lego/5.jpg" title="Amin Arzhang" subtitle="Frontend Developer">
        </v-list-item>
    </v-list>
    <v-divider></v-divider>
    <v-list density="compact" nav>
        <v-list-item prepend-icon="mdi-image" title="Color Gallery" value="color" @click="selectOption(true)"></v-list-item>
        <v-list-item prepend-icon="mdi-dialpad" title="Grayspace Gallery" value="color" @click="selectOption(false)"></v-list-item>
    </v-list>
  </v-navigation-drawer>  
</template>

<script>
export default {
    name: "SideBar",
    emits: ['selectOption'],
    setup(_, { emit }) {
        const selectOption = (isColor) => {
            emit('selectOption', isColor);
        };
        
        return {
            selectOption
        };
    }
}
</script>

