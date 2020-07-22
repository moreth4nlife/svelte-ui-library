<script>
  import { createEventDispatcher } from "svelte";

  let className = "";
  let placeholder = "";

  let primary = false;
  let secondary = false;
  let disabled = false;

  export { className as class, placeholder, primary, secondary, disabled };

  const dispatch = createEventDispatcher();

  const handleClick = () => {
    if (!disabled) {
      dispatch("click");
    }
  };
</script>

<style>
  button:disabled {
    cursor: default;
  }
  button {
    margin: 12px 12px;
    padding: 0.5rem 1rem;
    display: inline-flex;
    position: relative;
    align-items: center;
    justify-content: center;
    box-sizing: border-box;
    border: none;
    outline: none;
    font-size: 14px;
    font-weight: 500;
    line-height: 20px;
    letter-spacing: 0.25px;
    user-select: none;
    overflow: hidden;
    vertical-align: middle;
    will-change: transform, opacity;
    cursor: pointer;
    transition: all 0.5s ease;
  }
  .primary {
    background: #0d6efd;
  }
  .secondary {
    background: lightgoldenrodyellow;
  }
  .disabled {
    background: lightgrey;
  }
</style>

<button
  class={className}
  class:primary
  class:secondary
  class:disabled
  on:click={() => handleClick()}>
  {placeholder}
</button>
