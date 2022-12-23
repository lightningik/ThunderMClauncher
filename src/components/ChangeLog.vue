<template>
<div class="container">
  <div class="change-card">
    <div>

    </div>
  </div>

</div>
</template>

<script>
export default {
  name: "ChangeLog"
}
</script>

<style scoped>
@media(prefers-color-scheme: dark) {

  .change-card {
    border-radius: 50px;
    color: #BE83D4;
    background-color: #0f0f0f;
    box-shadow: 0 4px 8px 0 rgba(0, 0, 0, 0.2);
    font-family: "Montserrat", sans-serif;
    position: fixed;
    z-index: 1;
    bottom: 20px;
    right: 20px;
    padding: 0.5em;
    height: 400px;
    width: 500px;
  }
}
</style>