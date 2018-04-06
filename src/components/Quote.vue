<template>
    <div class="col-md-4">
        <div class="card quote">
             <div class="card-body">
               <slot></slot>
            </div>
        </div>
    </div>
</template>

<script>
export default {
  props: ["qoutes"]
};
</script>
<style>
.card-body {
  font-size: 24px;
  color: #6e6e6e;
}

.quote {
  cursor: pointer;
}

.quote:hover {
  background-color: #ffe2e2;
}
</style>
