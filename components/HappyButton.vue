<template>
  <button
    v-ripple
    :class="getClass">
    {{ label }}
  </button>
</template>
<script>
import Ripple from 'vue-ripple-directive';

export default {
  directives: {
    Ripple
  },
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
        case 'primary': {
          return 'primary';
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
  background-color: #f1f1f1;
  box-shadow: 0px 0px 45px -8px rgba(0,0,0,0.75);
  color: black;
  border: none;
  border-radius: 5px;
  font-size: 0.8em;
  padding: 10px 20px;
  transition: all ease-in-out 100ms;
  font-weight: 600;
  text-transform: uppercase;

  &:hover {
    background-color: darken(#f1f1f1, 5)
  }
  &:disabled {
    color: rgba(255,255,255,.75);
    background-color: grey;
    box-shadow: 0 15px 35px rgba(50,50,93,.1), 0 5px 15px rgba(0,0,0,.07);
  }
}

.danger {
  background-color: crimson;
  color: white;
  &:hover {
    background-color: darken(crimson, 5)
  }
}

.info {
  background-color: blueviolet;
  color: white;
  &:hover {
    background-color: darken(blueviolet, 5)
  }
}

.primary {
  background-color: orangered;
  color: white;
  &:hover {
    background-color: darken(orangered, 5)
  }
}
</style>


