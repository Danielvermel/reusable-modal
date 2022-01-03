<template>
  <div class="home">
    <Modal 
        :modalActive="modalActive" 
        class="modal-content"
    > 
        <h1>This is a Modal Header</h1> 
        <p>This is a modal message</p>
    </Modal>
    <button @click="toggleModal" type="button">Open Modal</button>
  </div>
</template>

<script>
import Modal from '@/components/Modal';
import {ref} from 'vue';

export default {
  name: 'Home',
  components: {
    Modal
  },
  setup () {
    const modalActive = ref(false);
    
    const toggleModal = () => {
        modalActive.value = !modalActive.value;
    }
    
    return {modalActive, toggleModal};
  }
}
</script>
