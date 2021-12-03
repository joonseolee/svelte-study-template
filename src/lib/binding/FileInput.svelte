<script>
  let files;
</script>

<label for="avatar">Upload a picture</label>
<input
  type="file"
  accept="image/png, image/jpeg"
  bind:files
  id="avatar"
  name="avatar"
/>

<label for="many">Upload mulitple files</label>
<input type="file" bind:files id="many" multiple />
