<script>
  import Richtext from "./Richtext.svelte";
  import { getData } from "./data.js";
  
  const initText = getData();
</script>

<Richtext {initText} />
