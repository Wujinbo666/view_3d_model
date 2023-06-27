<script setup>
import ThreeDModel from '.';
const url3D = 'http://rw8b8qdys.bkt.clouddn.com/m12asm.gltf'
</script>

<template>
  <div>
    <div class="wrapper">
      <span @click.stop="btnCloseHandler" class="btnClose">×</span>
        <ThreeDModel
        class="three-d-model"
        :file-path="url3D"
        :use-editor="false"
        :custom-settings="{
          autoRotate: false,
          exposure: 0.38,
          directionalLight: {
            intensity: 0.1,
            color: '#FFFFFF'
          },
          ambientLight: {
            intensity: 2,
            color: '#000'
          },
          fov: 70
        }"
      />
    </div>
  </div>
  <HelloWorld msg="Vite + Vue" />
</template>

<style scoped>
.wrapper {
  position: relative;
  height: 70vh;
  width: 60vw;
  background-color: #ffff;
  }

  .three-d-model {
      position: absolute;
      top: 50%;
      transform: translate(0,-50%);
      height: 100%;
      width: 100%;
      background: linear-gradient(#88c5ea, #fafdfe);
    }
    .btnClose {
      position: absolute;
      z-index: 2;
      right: 10px;
      cursor: pointer;
      font-size: 25px;
    }
</style>
