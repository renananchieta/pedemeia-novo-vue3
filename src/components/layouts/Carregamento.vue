<template>
    <div class="pa-4 text-center">
        <v-dialog
        v-model="dialog"
        max-width="320"
        persistent
        >
            <v-list
                class="py-2"
                color="primary"
                elevation="12"
                rounded="lg"
            >
                <v-list-item
                prepend-icon="$vuetify-outline"
                :title="mensagem"
                >
                <template v-slot:prepend>
                    <div class="pe-4">
                        <v-icon color="primary" size="x-large"></v-icon>
                    </div>
                </template>

                <template v-slot:append>
                    <v-progress-circular
                    color="primary"
                    indeterminate="disable-shrink"
                    size="16"
                    width="2"
                    ></v-progress-circular>
                </template>
                </v-list-item>
            </v-list>
        </v-dialog>
    </div>
</template>

<script setup>
import { ref } from 'vue';
/**
 * Props
 */
 const props = defineProps({
  // mensagem: {
  //   type: String,
  //   required: true,
  // },
  openDialog:{
    type: Boolean,
    default: false,
    required: true,
  }
});

/**
 * Data
 */
const dialog = ref(props.openDialog);

/**
 * Methods
 */
</script>