<script>
    import "@dhx/trial-richtext/codebase/richtext.min.css";
    import { onMount } from "svelte";
    import { Richtext } from "@dhx/trial-richtext";
    
    export let initText;

    let container;
    let richtext;
    onMount(() => {
        richtext = new Richtext(container, {});
        return () => {
            richtext.destructor();
        };
    });

    $: richtext?.setValue(initText, "markdown")
</script>

<div bind:this={container} style="width: 100%; height: 100%;">

</div>

