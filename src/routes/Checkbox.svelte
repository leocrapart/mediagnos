<script>
  export let name
  export let checked = false
</script>

<div>
<label>
  <input type=checkbox bind:checked={checked}>
  {name}
</label>
</div>
