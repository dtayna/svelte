<div class="questionPane">
	<button on:selection={e=> onSelection(0)}>
		TAB1
	</button>
	<button on:selection={e=> onSelection(1)}>
		TAB2
	</button>
	<button on:selection={e=> onSelection(2)}>
		TAB3
	</button>
	<button on:selection={e=> onSelection(3)}>
		TAB4
	</button>

	<Question {...conts[currentCont]} />
</div>



<script lang="ts">
		import Cont from "./Cont.svelte";

		const conts = [
		  {
		    statement: "Tab 111111"
		  },
		  {
		    statement: "Tab 22222222"
		  },
		  {
		    statement: "Tab 33333333"
		  },
		  {
		    statement: "Tab 4444444"
		  }
		];

		let currentCont = 0;

		function onSelection(option) {
		  currentCont = option;
		  console.log(`opção selecionada ${option}`);
		}
</script>