<script>
  const variants = {
    primary: "steelblue",
    info: "darkcyan",
    warning: "goldenrod",
    dark: "darkslategray",
    danger: "red"
  };
  export let variant = variants.primary;
</script>

<style lang="scss">
  button {
    color: white;
    background-color: steelblue;
    border: 1px solid;
    border-color: steelblue;
    border-radius: 4px;
    padding: 5px 15px;
    &.primary {
      background-color: steelblue;
    }
    &.info {
      background-color: darkcyan;
    }
  }
</style>

<button on:click class={variant}>
  <slot>button</slot>
</button>
