<template>
  <v-container fluid>
    <v-form>
      <v-file-input
        label="Selecione as legendas"
        outlined
        append-icon="mdi-send"
        mutiple
        chips
        v-model="files"
        @click:append-icon="processSubtitles"
      >
      </v-file-input>
    </v-form>
    <div class="pills">
      <Pill
        v-for="word in grupedWords"
        :key="word.name"
        :name="word.name"
        :amount="word.amount"
      />
    </div>
  </v-container>
</template>

<script>
import Pill from "./Pill.vue";
export default {
  components: { Pill },
  data: function() {
    return {
      files: [],
      grupedWords: [
        { name: "i", amount: 1860 },
        { name: "you", amount: 900 },
        { name: "he", amount: 860 },
      ],
    };
  },
  methods: {
    processSubtitles() {
      console.log(this.files);
    },
  },
};
</script>

<style>
.pills {
  display: flex;
  flex-wrap: wrap;
  justify-content: space-between;
}
</style>
