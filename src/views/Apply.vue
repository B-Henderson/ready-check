<template>
  <div class="app">
    <apply-form></apply-form>
  </div>
</template>
<script>
import ApplyForm from "@/components/Form.vue";
export default {
  components: { ApplyForm }
};
</script>
<style lang="scss">
.apply-container {
  display: flex;
  align-content: center;
  justify-content: center;
  flex-wrap: wrap;
}
</style>