<template>
  <div id="splash" v-bind:class="{ 'ease-out': easeOut }" v-if="show" class="fixed z-10 inset-0 overflow-y-auto" >
    <div
      class="flex items-center justify-center min-h-screen p-4 text-center sm:block sm:p-0"
    >
      <div class="fixed inset-0 transition-opacity" aria-hidden="true">
        <div class="absolute inset-0 bg-white"></div>
      </div>

      <span
        class="hidden sm:inline-block sm:align-middle sm:h-screen"
        aria-hidden="true"
        >&#8203;</span
      >
      <div
        class="inline-block transform transition-all align-middle max-w-lg"
        style="border-radius: 15px;"
        role="dialog"
        aria-modal="true"
        aria-labelledby="modal-headline"
      >
        <div class="p-6">
          <div class="flex items-center justify-center">
            <div
              class="mx-auto flex-shrink-0 flex items-center justify-center rounded-full sm:mx-0 h-full w-full"
            >
              <Icon />
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
<style scoped>
#splash {
  opacity: 1;
}

#splash.ease-out {
  transition: opacity .8s ease-in-out;
  opacity: 0;
}
</style>
<script lang="ts">
import Vue from 'vue';

const show: boolean = true;
const easeOut: boolean = false;

export default Vue.extend({
  data: function() {
    return {
      show, easeOut,
    }
  },
  created() {
    setTimeout(() => {
      this.easeOut = true
    }, 3000);

    setTimeout(() => {
      this.show = false
    }, 3800);
  },
})
</script>