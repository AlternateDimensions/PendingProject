<script>
	import FeedbackList from './components/FeedbackList.svelte';

	let feedback = [
		{
			id: 1,
			rating: 10,
			text: "This is pretty good",
		},
		{	id: 2,
			rating: 9,
			text: "This is not for me but still decent",
		},
		{
			id: 3,
			rating: 2,
			text: "What is this crap????",
		}
	]
	const deleteFeedback = (e) => {
		const itemId = e.detail
		feedback = feedback.filter((item) => item.id != itemId)

	}
</script>

<main class="container">
	<FeedbackList feedback={feedback} on:delete-feedback={deleteFeedback} />
</main>