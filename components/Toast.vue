<style lang="scss">
  .toast {
    position: fixed;
    bottom: 40px;
    left: 50%;
    transform: translateX(-50%);
    padding: 12px 16px;
    z-index: 1006;
    color: #fff;
    font-size: .95rem;
    letter-spacing: 1px;
    border-radius: 20px;

    &--info {
      background-color: $theme-color;
      box-shadow: 10px 20px 30px rgba(10, 132, 234, 0.5);
    }

    &--success {
      background-color: green;
      box-shadow: 10px 20px 30px rgba(28, 234, 37, 0.5);
    }

    &--warning {
      background-color: orange;
      box-shadow: 10px 20px 30px rgba(234, 200, 7, 0.5);
    }

    &--error {
      background-color: red;
      box-shadow: 10px 20px 30px rgba(234, 117, 28, 0.5);
    }

  }
</style>

<template>
  <transition name="fade">
    <div v-show="isShow" class="toast" :class="`toast--${type}`">
      <Icon v-if="icon" :name="icon"></Icon>
      <span class="text">{{ text }}</span>
    </div>
  </transition>
</template>

<script>
export default {
  name: 'Toast',
  data() {
    return {
      text: '',
      icon: 'info',
      type: 'info',
      isShow: false
    }
  },
  computed: {
    style() {
      return {}
    }
  },
  methods: {}
}
</script>
