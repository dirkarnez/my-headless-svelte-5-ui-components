<script>

	import Accordion from "./Accordion.svelte";
	import AccordionSection from "./AccordionSection.svelte";
  let activeSectionA;
	let activeSectionB;
</script>
<Accordion>
	<AccordionSection bind:activeSection={activeSectionA} index={0}>
		{#snippet name()}
			P. Sherman 1
		{/snippet}
		{#snippet address()}
			42 Wallaby Way<br />
			Sydney
		{/snippet}
	</AccordionSection>

		<AccordionSection bind:activeSection={activeSectionA} index={1}>
		{#snippet name()}
			P. Sherman 2
		{/snippet}
		{#snippet address()}
			42 Wallaby Way<br />
			Sydney
		{/snippet}
	</AccordionSection>
</Accordion>
<br>
<Accordion>
	<AccordionSection bind:activeSection={activeSectionB} index={0}>
		{#snippet name()}
			P. Sherman 1
		{/snippet}
		{#snippet address()}
			42 Wallaby Way<br />
			Sydney
		{/snippet}
	</AccordionSection>

		<AccordionSection bind:activeSection={activeSectionB} index={1}>
		{#snippet name()}
			P. Sherman 2
		{/snippet}
		{#snippet address()}
			42 Wallaby Way<br />
			Sydney
		{/snippet}
	</AccordionSection>
</Accordion>
