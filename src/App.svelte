<script>
import FeedbackForm from "./components/FeedbackForm.svelte";

	import FreedbackForm from "./components/FeedbackForm.svelte"
	import FeedbackList from "./components/FeedbackList.svelte"
	import FeedbackStat from "./components/FeedbackStat.svelte"
let feedback =[
	{
		id:'1',
		rating: 10,
		text: "this is awesome,this is awesomethis is awesomethis is awesomethis is awesomethis ithis is awesomethis is awesomethis is awesomethis is awesomethis is awesomethis is awesomethis is awesomethis is awesomes awesomethis is awesomethis is awesome"
	},
	{
		id:'2',
		rating: 9,
		text: "this is awesome,this is awesomethis is awesomethis is awesomethis is awesomethis ithis is awesomethis is awesomethis is awesomethis is awesomethis is awesomethis is awesomethis is awesomethis is awesomes awesomethis is awesomethis is awesome"
	},
	{
		id:'3',
		rating: 8,
		text: "this is awesome,this is awesomethis is awesomethis is awesomethis is awesomethis ithis is awesomethis is awesomethis is awesomethis is awesomethis is awesomethis is awesomethis is awesomethis is awesomes awesomethis is awesomethis is awesome"
	},
	{
		id:'4',
		rating: 7,
		text: "this is awesome,this is awesomethis is awesomethis is awesomethis is awesomethis ithis is awesomethis is awesomethis is awesomethis is awesomethis is awesomethis is awesomethis is awesomethis is awesomes awesomethis is awesomethis is awesome"
	},
	{
		id:'5',
		rating: 6,
		text: "this is awesome,this is awesomethis is awesomethis is awesomethis is awesomethis ithis is awesomethis is awesomethis is awesomethis is awesomethis is awesomethis is awesomethis is awesomethis is awesomes awesomethis is awesomethis is awesome"
	},
	{
		id:'6',
		rating: 5,
		text: "this is awesome,this is awesomethis is awesomethis is awesomethis is awesomethis ithis is awesomethis is awesomethis is awesomethis is awesomethis is awesomethis is awesomethis is awesomethis is awesomes awesomethis is awesomethis is awesome"
	},
]

$: count  = feedback.length
$: average = feedback.reduce((a, {rating}) => a + rating, 0)/feedback.length

const deleteFeedback = (e) =>{
	const itemId = e.detail

	feedback = feedback.filter((item) => item.id != itemId)
}
</script>

<main class='container'>
	<FeedbackForm />
	<FeedbackStat {count} {average} />
	<FeedbackList {feedback} on:delete={deleteFeedback} />
</main>
