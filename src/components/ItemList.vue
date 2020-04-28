<template>
  <div>
    <h1>ItemList</h1>
    <item
      day="8"
      num="1"
      quiz="xxx"
      realAnswer="yy"
    />
  </div>
</template>
<script lang="ts">
import { Component, Vue, Prop } from "vue-property-decorator";
import Item from "@/components/Item.vue";
@Component({
  components: {
    Item
  }
})
export default class ItemList extends Vue {}
</script>
