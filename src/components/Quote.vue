<template>
  <div class="col-sm-12 col-md-6 col-lg-3">
    <div class="panel panel-default">
      <div class="panel-body quote">
        <slot></slot>
      </div>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style scoped>
.panel-body {
  font-family: "Arizonia", sans-serif;
  font-size: 24px;
  color: #aaa;
}

.quote {
  cursor: pointer;
}

.quote:hover {
  background-color: rgba(255, 192, 203, 0.727);
}
</style>