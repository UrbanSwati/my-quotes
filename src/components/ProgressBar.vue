<template>
    <div class="progress">
        <div class="progress-bar" role="progressbar" :style="{width: (qoutes.length * 10) + '%'}" aria-valuenow="25" aria-valuemin="0" aria-valuemax="100">{{qoutes.length}} / {{maxQuotes}}</div>
    </div>
</template>

<script>
export default {
  props: ["qoutes", "maxQuotes"]
};
</script>
<style>

</style>
