<script>
	let { activeSection = $bindable(), name, address, email, index  } = $props();
</script>
<button type="button" style={" width: 100%;"} onclick={() => {activeSection = index;}}>
	Section {index}
</button>
<div style={`width: 100%; display: ${activeSection === index ? 'block' : 'none'}`}>
	{@render name()}
</div>

    
  
