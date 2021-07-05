<script>
	import { jsPDF } from 'jspdf';

	// Default export is a4 paper, portrait, using millimeters for units
	const doc = new jsPDF();

	doc.text('Hello world!', 10, 10);
	const downloadPdf = () => {
		doc.save('a4.pdf');
	};
</script>

<svelte:head>
	<title>Elternbrief</title>
</svelte:head>

<h1 class="text-4xl text-center my-8">Willkommen beim Elternbrief-Generator</h1>
<button
	class="bg-blue-500 hover:bg-blue-700 text-white font-bold py-2 px-4 rounded"
	on:click={downloadPdf}>Download PDF</button
>
