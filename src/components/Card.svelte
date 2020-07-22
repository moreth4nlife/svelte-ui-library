<script>
  let placeholder = "";

  export { placeholder };
</script>

<style>
  .card-wrapper {
    width: 100%;
    border-radius: 15px;
    box-shadow: 0 1px 2px rgba(0, 0, 0, 0.07), 0 2px 4px rgba(0, 0, 0, 0.07),
      0 4px 8px rgba(0, 0, 0, 0.07), 0 8px 16px rgba(0, 0, 0, 0.07),
      0 16px 32px rgba(0, 0, 0, 0.07), 0 32px 64px rgba(0, 0, 0, 0.07);
    background: white;
  }
  .card-header,
  .card-body,
  .card-footer {
    padding: 1rem;
  }
</style>

<div class="card-wrapper">
  <div class="card-header">
    <slot name="card-header" />
  </div>
  <div class="card-body">
    <slot name="card-body">{placeholder}</slot>
  </div>
  <div class="card-footer">
    <slot name="card-footer" />
  </div>
</div>
