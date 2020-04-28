<template>
  <div>
    <label>{{this.num}}.{{this.quiz}}: </label>
    <input
      v-model="answer"
      size=100
    />
  </div>
</template>
<script lang="ts">
import { Component, Vue, Prop } from "vue-property-decorator";

@Component
export default class Item extends Vue {
  @Prop({ type: String, required: true }) readonly quiz!: string;
  @Prop({ type: String, required: true }) readonly realAnswer!: string;
  @Prop({ type: Number, required: true }) readonly num!: number;

  private answer!: string;
  created() {
    this.answer = this.realAnswer;
  }
}
</script>
