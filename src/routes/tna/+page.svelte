<script lang="ts">
	type Question = {
		question: string;
		answers: string[];
		correctAnswer: string;
	};

	let questions = [] as Question[];

	let newQuestion: Question = { question: '', answers: [], correctAnswer: '' };

	let newQuestionString = '';

	const addQuestion = () => {
		newQuestion.question = newQuestionString;
		newQuestion.correctAnswer = '';
		questions = [...questions, newQuestion];
		newQuestion = { question: '', answers: [], correctAnswer: '' };
	};
</script>

<br />
<h1>TNA</h1>

<div class="w-full flex" style=" padding: 1rem; ">
	<div class="w-1/2">
		<input
			class="rounded-md"
			type="text"
			name="question"
			bind:value={newQuestionString}
			placeholder="Enter Assessment"
		/>

		{#if newQuestion.answers.length > 0}
			{#each newQuestion.answers as answer, i}
				<div>
					<!-- svelte-ignore a11y-label-has-associated-control -->
					<label>{answer}</label>
				</div>
			{/each}
		{/if}
		<br />
		<br />
		<button class="btn btn-sm variant-ghost-surface" type="button" on:click={addQuestion}
			>Add Assessment</button
		>
	</div>
	<div>
		<h1>Assessment</h1>
		{#if questions.length > 0}
			{#each questions as question, i}
				<div>
					<h2>{question.question}</h2>
					{#each question.answers as answer, i}
						<div>
							<!-- svelte-ignore a11y-label-has-associated-control -->
							<label>{answer}</label>
						</div>
					{/each}
				</div>
			{/each}
		{/if}
	</div>
</div>

<style>
	h1 {
		font-size: 2rem;
	}
</style>
