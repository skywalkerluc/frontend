<template>
  <div class="happy-card">
    <slot name="box-1" />
    <slot name="box-2" />
    <slot name="box-3" />
  </div>
</template>
<script>
export default {

}
</script>
<style lang="scss" scoped>
.happy-card {
  padding: 20px;
  border: 1px solid rgba(111, 109, 134, 0.25);
  background-color: aliceblue;
  display: flex;
  border-radius: 20px;

  * {
    margin-right: 10px;
  }
}
</style>


