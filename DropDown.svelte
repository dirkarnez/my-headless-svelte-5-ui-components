<script>
		let { open = false, children } = $props();
</script>

<div style={"position: relative;"}>
  <button onclick={() => {  open = !open }}>Dropdown</button>
  <div style={`display: ${open ? "block": "none"}; position: absolute; z-index: 1;`}>
		{@render children()}
  </div>
</div>
