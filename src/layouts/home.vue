<template>
  <main class="paper">
    <div class="centered index-page">
      <RouterView />
    </div>
  </main>
</template>

<style scoped>
.paper {
  display: grid;
  position: absolute;
  left: 0;
  top:0;
  right: 0;
  bottom: 0;
  place-items: center;
  user-select: none;
  justify-content: center;
}
.centered {
    position: fixed;
    top: 50%;
    left: 50%;
    transform: translate(-50%,-50%);
}
.index-page {
    max-height: 100%;
    padding: 60px 40px 30px;
    overflow: auto;
    width: 100%;
}
@media (min-width: 768px) {
  .index-page {
      width: auto;
  }
}
</style>
