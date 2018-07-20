<template>
  <div class="happy-card">
    <span class="happy-card--title">{{ title }}</span>
    <div class="happy-card--content">
      <p class="happy-card--content--resume">{{ resume }}</p>
      <img
        v-if="image"
        :src="image"
        class="happy-card--content--image"
      >
    </div>
    <div
      v-if="$slots.footer"
      class="happy-card--footer">
      <slot name="footer"/>
    </div>
  </div>
</template>
<script>
export default {
  props: {
    title: {
      type: String,
      required: true
    },
    resume: {
      type: String,
      default: ''
    },
    image: {
      type: String,
      default: ''
    }
  }
}
</script>
<style lang="scss" scoped>
.happy-card {
  padding: 20px;
  box-shadow: 0 15px 35px rgba(50,50,93,.1), 0 5px 15px rgba(0,0,0,.07);
  background-color: #fff;
  display: flex;
  flex-direction: column;
  border-radius: 5px;

  &--title {
    font-weight: 600;
  }
  &--content {
    display: flex;
    align-items: center;

    &--resume {
      font-weight: 300;
      flex-grow: 1;
      word-break: break-all;
    }
    &--image {
      width: 64px;
      height: 64px;
      border-radius: 10px;
    }
  }
  &--footer {
    border-top: 1px solid rgba(0,0,0,.07);
    padding-top: 20px;
    margin-top: 20px;
  }
}
</style>


