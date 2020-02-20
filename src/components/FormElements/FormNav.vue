<template>
  <div>
    <form-progress />
    <div class="nav">
      <div class="form-button" @click="$emit('back')">
        <img src="../../assets/icons/arrowDark.svg" />
      </div>
      <div class="form-button" style="background-color:black;" @click="$emit('next')">
        <img src="../../assets/icons/arrowLight.svg" />
      </div>
    </div>
  </div>
</template>
<script>
import FormProgress from "./FormProgress.vue"
export default {
  name: "form-nav",
  components: {
    "form-progress": FormProgress
  }
}
</script>
