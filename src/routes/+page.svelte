<script>
	import Checkbox from './Checkbox.svelte'

	let showInfarctus = false


	let sueurs = true
	let febriculeRetardee24h = true
	let agitation = true
	let nausees = true 
	let vomissements = true 
	let troublesDuRhytme = true
	let plusDePressionArterielle = true

	let dSpontanee = true 
	let dRepos = true
	let dBrutale = true
	let dConstrictive = true
	let dBrulure = true
	let dPrecordiale = true
	let dRetrosteralle = true
	let dIrradiantBrasGauche_Machoire_Epigastre_Poignet = true
	let dIntorso = true
	let dDurable = true
	let dTrepsine = true


	$: allSymptomes = sueurs && febriculeRetardee24h && agitation && nausees && vomissements && troublesDuRhytme && plusDePressionArterielle

	$: allDouleurs = dSpontanee && dRepos && dBrutale && dConstrictive && dBrulure && dPrecordiale && dRetrosteralle && dIrradiantBrasGauche_Machoire_Epigastre_Poignet && dIntorso && dDurable && dTrepsine

	$: if (allDouleurs && allSymptomes) {
		showInfarctus = true
		}
	   else {
	   	showInfarctus = false
	   }
</script>

<div class="py-3"></div>


<div class="flex justify-center">
	<div>
		<!-- debug -->
		<!-- <div>allSymptomes {allSymptomes}</div>
		<div>allDouleurs {allDouleurs}</div>
		<div>
		<label>
		  <input type=checkbox bind:checked={showInfarctus}>
		  infarctus {showInfarctus}
		</label>
		</div> -->


		<div class="font-bold">symptomes</div>
		<!-- radio btn for symptoms -->

		<div>
		<label>
		  <input type=checkbox bind:checked={sueurs}>
		  sueurs
		</label>
		</div>
		<div>
		<label>
		  <input type=checkbox bind:checked={febriculeRetardee24h}>
		  febricule retardée (+24h)
		</label>
		</div>
		<div>
		<label>
		  <input type=checkbox bind:checked={agitation}>
		  agitation
		</label>
		</div>
		<div>
		<label>
		  <input type=checkbox bind:checked={nausees}>
		  nausées
		</label>
		</div>
		<div>
		<label>
		  <input type=checkbox bind:checked={vomissements}>
		  vomissements
		</label>
		</div>
		<div>
		<label>
		  <input type=checkbox bind:checked={troublesDuRhytme}>
		  troubles du rhytme
		</label>
		</div>
		<div>
		<label>
		  <input type=checkbox bind:checked={plusDePressionArterielle}>
		  plus de pression arterielle
		</label>
		</div>


		<div class="py-3"></div>

		<div class="font-bold">douleurs</div>

		<div>
		<label>
		  <input type=checkbox bind:checked={dSpontanee}>
		  spontanée
		</label>
		</div>

		<div>
		<label>
		  <input type=checkbox bind:checked={dRepos}>
		  au repos
		</label>
		</div>

		<div>
		<label>
		  <input type=checkbox bind:checked={dBrutale}>
		  brutale
		</label>
		</div>

		<div>
		<label>
		  <input type=checkbox bind:checked={dConstrictive}>
		  constrictive
		</label>
		</div>

		<div>
		<label>
		  <input type=checkbox bind:checked={dBrulure}>
		  brulure
		</label>
		</div>

		<div>
		<label>
		  <input type=checkbox bind:checked={dPrecordiale}>
		  précordiale
		</label>
		</div>

		<div>
		<label>
		  <input type=checkbox bind:checked={dRetrosteralle}>
		  retrostéralle
		</label>
		</div>

		<div>
		<label>
		  <input type=checkbox bind:checked={dIrradiantBrasGauche_Machoire_Epigastre_Poignet}>
		  irradiant bras grauche/machoire/epigastre/poignet
		</label>
		</div>

		<div>
		<label>
		  <input type=checkbox bind:checked={dIntorso}>
		  intorso (sentiment de mort imminente)
		</label>
		</div>

		<div>
		<label>
		  <input type=checkbox bind:checked={dDurable}>
		  durable (+ de 20 min)
		</label>
		</div>

		<div>
		<label>
		  <input type=checkbox bind:checked={dTrepsine}>
		  trépsine inutile
		</label>
		</div>


		{#if showInfarctus}

		<div class="py-3"></div>
		<div class="text-3xl">infarctus</div>
		<div class="py-3"></div>


		<div class="font-bold">fiche reflexe</div>
		<div>-faire ecg</div>
		<div>-biolope : + CPRF(MB) + tropamine Tou I</div>
		<div>-echographie</div>
		<div>-coronarographie</div>

		<div class="py-3"></div>


		<div class="font-bold">risques</div>
		<div>-trouble rythme</div>
		<div>-mort subite</div>
		<div>-collapsus</div>
		<div>-OAP</div>
		<div>-Embolie pulmonaire / thrombose </div>
		<div>artérielle (membre inférieur/cerveau)</div>

		{/if}
	</div>
</div>
