<script>
	import { SliceSimulator } from "@slicemachine/adapter-sveltekit/simulator";

	/** @type {import("@prismicio/client").Content.ImageSlice} */
	export let slice;

	console.log(slice)
</script>

<section data-slice-type={slice.slice_type} data-slice-variation={slice.variation}>

	<img src={slice.primary.image.url} alt="">
	<p class="naam">{slice.primary.name[0].text}</p>
	<p class="title">{slice.primary.title[0].text} 
	</p>
	<p class="opleidingen">Opleidingen:</p>
	<p class="opleiding2">{slice.primary.opleiding[0].text}</p>
	<p class="opleiding3">{slice.primary.opleiding2[0].text}</p>
</section>


<style>
img{
	display: flex;
	width: 20%;
	margin-left: 20%;
	padding-left: 200px;
	padding-right: 200px;
	padding-top: 50px;
	padding-bottom: 50px;
	background-color: black;
	margin-top: 50px;

	border-top-left-radius: 20px;
	border-top-right-radius: 20px;

	/* border-style: solid;
	border-width: 2px;
	border-color: gold;
	 */
	
}

.naam{
	background-color: black;
	display: flex;
	justify-content: center;
	color: gold;
	font-size: 25px;
	
	padding: 20px;
	border-radius: 20px;
	margin-left: 150px;
	margin-right: 150px;

	border-style: solid;
	border-width: 2px;
	border-color: gold;
}

.title{
	background-color: black;
	display: flex;
	justify-content: center;
	color: gold;	

	margin: 0;
	padding: 20px;

	border-radius: 20px;

	margin-left: 150px;
	margin-right: 150px;
}

.opleidingen{
	background-color: black;
	display: flex;
	justify-content: center;
	color: rgb(190, 91, 25);
	font-size: 25px;
	margin: 10px;
	padding: 20px;
	border-radius: 20px;
	margin-left: 150px;
	margin-right: 150px;

	border-style: solid;
	border-width: 2px;
	border-color: rgb(190, 91, 25);
}

.opleiding2{
	background-color: black;
	display: flex;
	justify-content: center;
	color: gold;	

	margin: 0;
	padding: 20px;
	
	margin-left: 150px;
	margin-right: 150px;
}

.opleiding3{
	background-color: black;
	display: flex;
	justify-content: center;
	color: gold;	

	margin: 0;
	padding: 20px;

	margin-left: 150px;
	margin-right: 150px;
}

</style>