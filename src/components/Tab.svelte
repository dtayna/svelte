<div class="questionPane">
	<button on:click={e=> onSelection(0)}>
		TAB1
	</button>
	<button on:click={e=> onSelection(1)}>
		TAB2
	</button>
	<button on:click={e=> onSelection(2)}>
		TAB3
	</button>
	<button on:click={e=> onSelection(3)}>
		TAB4
	</button>
	<div class="conteudo">
		<Cont {...conts[currentCont]} />
	</div>
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

		function onSelection(x) {
		  currentCont = x;
		  console.log(`opção selecionada ${x}`);
		}
</script>

<style>
		.conteudo {
		  padding: 20px;
		  margin: 10px 0;
		  border-radius: 10px;
		  border: 1px solid #aaa;
		  background-color: #f0f0f0;
		}
</style>