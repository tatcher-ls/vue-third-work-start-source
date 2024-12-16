<template>
  <div>Demo 4</div>
  <demo-container>
    <div class="counter">
      <counter-button
          :disabled="counterStore.isDecrementDisabled"
          @action="counterStore.decrement"
      >
        -
      </counter-button>

      <counter-value :value="counterStore.value"/>

      <counter-button
          @action="counterStore.increment"
      >
        +
      </counter-button>
    </div>
  </demo-container>
</template>

<script setup>
import {ref} from "vue";
import CounterButton from "./CounterButton.vue";
import CounterValue from "@/demo1/CounterValue.vue";
import DemoContainer from "@/components/DemoContainer.vue";
import {useCounterStore} from "./store";

const count = ref(0);

const counterStore = useCounterStore()

</script>


<style lang="scss" scoped>
.counter {
  display: flex;
  align-items: center;
}
</style>
