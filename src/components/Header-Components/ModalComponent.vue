<template>
  <div class="modal" v-show="show">
    <div :style="modalContentStyle">
      <div class="d-flex justify-content-end">
        <span class="close" @click="close">&times;</span>
      </div>
      <slot></slot>
    </div>
  </div>
</template>

<script>
export default {
  name: 'ModalComponent',
  props: {
    show: Boolean,
    modalContentStyle: String
  },
  methods: {
    close() {
      this.$emit('close')
    },
    updated() {
      console.log('Component updated')
    }
  }
}
</script>

<style scoped>
/* Styles for the modal component */
.modal {
  display: block;
  position: fixed;
  z-index: 999;
  left: 0;
  top: 0;
  width: 100%;
  height: 100%;
  overflow: auto;
  background-color: rgba(249, 249, 249, 0.48);
}

.close {
  color: white;
  background-color: #F023B5;
  font-size: 28px;
  font-weight: bold;
  margin-top: 5px;
  margin-right: -120px;
  width: 40px;
  height: 40px;
  text-align: center;
  border-radius: 50%;
  display: flex;
  align-items: center;
  justify-content: center;
}

.close:hover,
.close:focus {
  background-color: #00BCD4;
  text-decoration: none;
  cursor: pointer;
}

</style>
