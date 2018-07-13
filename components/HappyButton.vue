<template>
  <button :class="getClass">{{ label }}</button>
</template>
<script>
export default {
  props: {
    label: {
      required: true,
      type: String
    },
    type: {
      required: false,
      type: String,
      default: ''
    }
  },
  computed: {
    getClass() {
      switch (this.type) {
        case 'danger': {
          return 'danger';
          break;
        }
        case 'info': {
          return 'info';
          break;
        }
        default: {
          return '';
        }
      }
    }
  }
}
</script>
<style lang="scss" scoped>
button {
  background-color: orangered;
  box-shadow: 0px 0px 45px -8px rgba(0,0,0,0.75);
  color: white;
  border: none;
  border-radius: 20px;
  font-size: 0.9em;
  padding: 10px 20px;
  transition: all ease-in-out 100ms;

  &:hover {
    background-color: darken(orangered, 10)
  }
}

.danger {
  background-color: crimson;
  &:hover {
    background-color: darken(crimson, 10)
  }
}

.info {
  background-color: blueviolet;
  &:hover {
    background-color: darken(blueviolet, 10)
  }
}
</style>


