<script>
	import { SliceSimulator } from "@slicemachine/adapter-sveltekit/simulator";

	/** @type {import("@prismicio/client").Content.ImageSlice} */
	export let slice;

	console.log(slice)
</script>

<section data-slice-type={slice.slice_type} data-slice-variation={slice.variation}>
	<article>
		<img src={slice.primary.image.url} alt="">
		<p class="naam">{slice.primary.name[0].text}</p>
	</article>
	
	<article>
		<p class="title">Hallo allemaal, mijn naam is Mohamed en ik ben 23 jaar. Ik volg de studie frontend & design op het HVA
			en werk daarnaast als junior IT systeembeheerder bij vincent TV producties. Mijn hobbys zijn gamen gymmen en ga vaak uit eten met vrienden of familie.

		</p>
		
	</article>

	<article>
		<p class="opleidingen">Opleidingen</p>
		<p class="opleiding2">{slice.primary.opleiding[0].text}</p>
		<p class="opleiding3">{slice.primary.opleiding2[0].text}</p>
	</article>
</section>


<style>
:root{
	--primary: black;
	--secondary: gold;
	--tertiary: white;
}

img{
	display: flex;
	width: 20%;
	margin-left: 20%;
	padding-left: 200px;
	padding-right: 200px;
	padding-top: 50px;
	padding-bottom: 50px;
	background-color: var(--primary);
	margin-top: 50px;

	border-top-left-radius: 20px;
	border-top-right-radius: 20px;

	/* border-style: solid;
	border-width: 2px;
	border-color: gold;
	 */
	
}

.naam{
	background-color: var(--primary);
	display: flex;
	justify-content: center;
	color: var(--secondary);
	font-size: 25px;
	
	padding: 20px;
	border-radius: 20px;
	margin-left: 150px;
	margin-right: 150px;
	margin-top: 0px;
	margin-bottom: 0px;

	border-style: solid;
	border-width: 1px;
	border-color: var(--secondary);
}

.title{
	background-color: var(--primary);
	display: flex;
	justify-content: center;
	color: var(--tertiary);	

	margin: 0;
	padding: 20px;

	border-radius: 10px;

	margin-left: 150px;
	margin-right: 150px;
}

.opleidingen{
	background-color: var(--primary);
	display: flex;
	justify-content: center;
	color: var(--secondary);
	font-size: 25px;
	margin: 10px;
	padding: 20px;
	border-radius: 20px;
	margin-left: 150px;
	margin-right: 150px;

	border-style: solid;
	border-width: 1px;
	border-color: var(--secondary);
}

.opleiding2{
	background-color: var(--primary);
	display: flex;
	justify-content: center;
	color: var(--tertiary);	

	margin: 0;
	padding: 20px;
	
	margin-left: 150px;
	margin-right: 150px;
}

.opleiding3{
	background-color: var(--primary);
	display: flex;
	justify-content: center;
	color: var(--tertiary);	

	margin: 0;
	padding: 20px;

	margin-left: 150px;
	margin-right: 150px;
}

.naam:hover{
  animation-name: scale;
  animation-duration: 5s;
  animation-iteration-count: 5;
}

.opleidingen:hover{
  animation-name: scale;
  animation-duration: 5s;
  animation-iteration-count: 5;
}

@keyframes scale {
0%{
  scale: 1;
}
50%{
  scale: 1.1;
}
100% {
    scale: 1;
  }
}

</style>