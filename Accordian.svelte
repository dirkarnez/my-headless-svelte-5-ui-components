<script>
  // State to manage the currently active section
  let activeSection = null;

  // Function to toggle the active section
  function toggleSection(section) {
    activeSection = activeSection === section ? null : section;
  }
</script>

<style>
  .accordion {
    background-color: #eee;
    color: #444;
    cursor: pointer;
    padding: 18px;
    width: 100%;
    border: none;
    text-align: left;
    outline: none;
    font-size: 15px;
    transition: 0.4s;
  }

  .active, .accordion:hover {
    background-color: #ccc; 
  }

  .panel {
    padding: 0 18px;
    display: none;
    background-color: white;
    overflow: hidden;
  }

  .panel.show {
    display: block;
  }
</style>

<h2>Accordion</h2>

{#each [1, 2, 3] as section}
  <button class="accordion {activeSection === section ? 'active' : ''}" on:click={() => toggleSection(section)}>
    Section {section}
  </button>
  <div class="panel {activeSection === section ? 'show' : ''}">
    <p>
      Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. 
      Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.
    </p>
  </div>
{/each}
