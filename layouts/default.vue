<template>
  <div class="flex flex-col h-screen w-screen">
    <!--
      Navigation Bar

      PARAMETERS
      :logoURL  (URL for Logo)
     -->
    <NaviWrapper
      imgURL="/img/lead-white-logo.png"
      ></NaviWrapper>

    <div class='flex-1'>
      <div class='flex'>
        <Nuxt class="w-full h-screen overflow-y-auto" />
      </div>
    </div>
    <FooterWrapper />
  </div>
</template>
<script>
export default {
}
</script>