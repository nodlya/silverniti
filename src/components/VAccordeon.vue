<template>
  <accordion-list>
    <accordion-item>
      <template #summary>Item summary</template>
      <template #icon>Icon Here</template>
      <h3>Main content</h3>
    </accordion-item>
    <accordion-item>
      <template #summary>Item summary</template>
      <template #icon>
        <img src="../assets/arrow_down.svg" />
      </template>
      <h3>Main content</h3>
    </accordion-item>
  </accordion-list>
</template>

<script>
import { AccordionList, AccordionItem } from "vue3-rich-accordion";

export default {
  name: "VAccordeon",
  components: { AccordionList, AccordionItem }
};
</script>

<style scoped>
.title {
  cursor: pointer;
  display: flex;
  justify-content: space-between;
}

.title,
.description {
  border: 1px solid black;
  padding: 5px;
}
</style>
