<style lang="scss">
  $h: 60px;
  $w: 200px;
  button {
    position: relative;
    height: $h;
    width: $w;
    border: none;
    background-color: steelblue;
    color: white;
    font-size: 24px;
    letter-spacing: 3px;
    transition: 1s;
    overflow: hidden;
    &::before {
      content: "";
      position: absolute;
      top: 0;
      left: -150px;
      width: 30%;
      height: 100%;
      background-color: white;
      filter: blur(40px);
      transform: skewX(-30deg);
      transition: 1s;
    }
    &:hover::before {
      left: $w + 150px;
    }
    &:hover {
      background-color: darkslategrey;
    }
  }
</style>

<button>Button</button>
