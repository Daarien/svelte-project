<style type="text/scss">
  $w: 200px;
  $h: 60px;
  button {
    position: relative;
    width: $w;
    height: $h;
    border: none;
    margin: 0;
    background-color: #fff;
    color: #00bfff;
    font-size: 24px;
    font-weight: 500;
    letter-spacing: 3px;
    transition: 2s;
    svg,
    rect {
      position: absolute;
      width: 100%;
      height: 100%;
      top: 0;
      left: 0;
    }
    rect {
      fill: none;
      stroke: #00bfff;
      stroke-width: 7px;
      stroke-dasharray: $h $w;
      stroke-dashoffset: 2 * $w + 2 * $h + $h / 2;
      transition: 2s;
    }
    &:hover {
      color: forestgreen;
      rect {
        stroke: forestgreen;
        stroke-dashoffset: $h + $h/2;
      }
    }
  }
</style>

<button>
  <svg>
    <rect />
  </svg>
  Button
</button>
