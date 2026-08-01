<script setup>
import modal from './ModalChild.vue'
import { ref } from 'vue'
import { defineExpose } from 'vue';
const showModal = ref(false)
const header = ref('Loading...');
const body1 = ref('Loading...');
const body2 = ref('Loading...');
const body3 = ref('Loading...');
const body4 = ref('Loading...');
const body5 = ref('Loading...');
const body6 = ref('Loading...');
const header1 = ref('Loading...');
const header2 = ref('Loading...');
const header3 = ref('Loading...');
const header4 = ref('Loading...');
const header5 = ref('Loading...');
const header6 = ref('Loading...');
const backgroundColour = ref('#69ccc971');
const colour = ref('white');
const openModal = () => {
  showModal.value = true;
};
const Pop = ref(null);
const openPopup = () => {
  Pop.value.openModal();
  closeModal();
};
defineExpose({
  openModal,
});
</script>
<template>
  <Teleport to="body">
    <modal :show="showModal" @close="showModal = false">
      <template #header>
        <h3 style="color: white;">Terms & Conditions</h3>
      </template>
      <template #body>
        <h2 style="font-weight:bold">1. Prices & Payment</h2>
        <h3>All pricing is subject to change at any time, without prior notice, and at the sole discretion of the service operator.</h3>
        <h2 style="font-weight:bold">2. Disclaimer of Warranties & Limitation of Liability</h2>
        <h3>Use of the service is undertaken at the user's sole risk. The service is provided on an as is, where is, and as available basis without warranties of any kind, express or implied. To the fullest extent permissible under applicable law, the operator expressly disclaims all warranties, including, but not limited to, implied warranties of merchantability, fitness for a particular purpose, and non-infringement. The operator does not warrant that the service will be uninterrupted, error-free, secure, or free from viruses or other harmful components. Under no circumstances shall the operator be liable for any direct, indirect, incidental, consequential, special, punitive, or exemplary damages arising out of or in connection with your access to or use of, or inability to access or use, the service, even if advised of the possibility of such damages.</h3>
        <h2 style="font-weight:bold">3. Modification of Terms</h2>
        <h3>We reserve the right to update, modify, or otherwise alter these Terms of Service at any time, without prior notice. Your continued use of the service following any changes constitutes your acceptance of the revised terms.
          Use of this service constitutes agreement to our Terms of Service. Service provided 'as-is' with no warranties expressed or implied.</h3>
      </template>
      <template #footer>
        <button @click="showModal = false" style="background-color:black;">Close</button>
      </template>
    </modal>
  </Teleport>
</template>