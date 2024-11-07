<template>
  <ul class="task__tags">
    <li v-for="(tag, index) in tags" :key="index">
      <span class="task__tag"> {{ tag }} </span>
    </li>
  </ul>
</template>

<script lang="ts" setup>
interface Props {
  tags: Array<string>;
}

defineProps<Props>();
</script>

<style lang="scss" scoped>
@import "@/assets/scss/app.scss";

.task__tags {
  display: flex;
  flex-wrap: wrap;

  width: 100%;

  @include clear-list;

  margin-top: 5px;

  li {
    margin-top: 4px;
    margin-right: 4px;
  }
}

.task__tag {
  padding: 4px 8px;

  color: $black-900;
  border-radius: 10px;
  background-color: $blue-gray-100;

  @include r-s10-h12;
}
</style>
