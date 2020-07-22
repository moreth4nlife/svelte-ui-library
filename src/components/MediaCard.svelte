<script>
  let placeholder = "";
  let imagePath = "";
  let alt = "";

  export { placeholder, imagePath, alt };
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
  .card-body {
    padding: 1rem;
  }
  .card-media {
    padding: 0;
    border-radius: 15px 15px 0 0;
    min-height: 180px;
    background-color: lightgrey;
  }
  .card-media img {
    width: 100%;
    height: 100%;
    object-fit: contain;
  }
</style>

<div class="card-wrapper">
  <div class="card-media">
    <img src={imagePath ? imagePath : '/static/images/default.png'} {alt} />
  </div>
  <div class="card-body">
    <slot name="card-body">{placeholder}</slot>
  </div>
</div>
