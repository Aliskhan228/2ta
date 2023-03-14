<template>
  <a-back-top class="back-to-top">
    <div class="ant-back-top-inner">
      <IconArrowUp />
    </div>
  </a-back-top>
  <div class="contact">
    <IconMessage />
  </div>
</template>
<script>
import IconMessage from "./icons/IconMessage.vue";
import IconArrowUp from "./icons/IconArrowUp.vue";
export default {
  components: { IconMessage, IconArrowUp },
};
</script>
