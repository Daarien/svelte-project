<style lang="scss">
  button {
    font-size: 24px;
    font-weight: 500;
    letter-spacing: 3px;
    color: #dcddd8;
    background-color: darkolivegreen;
    width: 200px;
    height: 60px;
    filter: blur(1px);
    transition: 300ms;
    span {
      position: relative;
      &::before,
      &::after {
        content: attr(data-content);
        position: absolute;
        left: 0;
        z-index: -1;
      }
      &::before {
        color: #dd0a35;
        animation: glitch 2s infinite;
      }
      &::after {
        content: attr(data-content);
        color: #1687a7;
        animation: glitch 2s reverse infinite;
      }
      @keyframes glitch {
        0% {
          transform: translate(0);
        }
        20% {
          transform: translate(-2px, 2px);
        }
        40% {
          transform: translate(-2px, -2px);
        }
        60% {
          transform: translate(2px, 2px);
        }
        80% {
          transform: translate(2px, -2px);
        }
        100% {
          transform: translate(0);
        }
      }
    }
    &:hover {
      background-color: darkslategray;
    }
  }
</style>

<button>
  <span data-content="Button">Button</span>
</button>
