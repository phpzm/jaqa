<template>
  <div>
    <div class="form-label">
      <span>{{ label }} {{ validator ? '*' : '' }}</span>
      <small>{{ ( error ? error : '') }}</small>
    </div>
  </div>
</template>

<script type="text/javascript">
  export default {
    name: 'f-label',
    props: ['label', 'validator', 'error']
  }
</script>
