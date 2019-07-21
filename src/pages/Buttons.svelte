<script>
  import DashedButton from "../comp/buttons/AnimBorderButton.svelte";
  import GlaringButton from "../comp/buttons/GlaringButton.svelte";
  import GlitchingButton from "../comp/buttons/GlitchingButton.svelte";
</script>

<style type="text/scss">
  :global(button) {
    cursor: pointer;
  }
  div {
    display: flex;
    section {
      margin: 0 2rem;
    }
  }
</style>

<div>
  <section>
    <DashedButton />
  </section>
  <section>
    <GlaringButton />
  </section>
  <section>
    <GlitchingButton />
  </section>
</div>
