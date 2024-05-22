<template>
  <section class="candidates" id="candidatura" aria-labelledby="CandidatesTitle" style="background-image: url(/images/candidates.jpg)">
    <div class="container padded">
      <h2 id="CandidatesTitle" class="font-headline skew">Vicent<br>Marzà</h2>
      <p class="candidates-description">Candidat al Parlament Europeu</p>
      <SiteSocials
          class="candidate-socials"
          :socials="[
            { icon: 'fa6-brands:instagram', name: 'Instagram', url: 'https://www.instagram.com/vicentmarza/' },
            { icon: 'fa6-brands:tiktok', name: 'TikTok', url: 'https://www.tiktok.com/@vicentmarza' },
            { icon: 'fa6-brands:x-twitter', name: 'Twitter / X', url: 'https://x.com/VicentMarza' },
          ]"
        />

      <div class="candidates-letter">
        <p>Els últims 8 anys, he fet tant com he pogut i més per representar les polítiques de Compromís a les Corts Valencianes i al Govern del Botànic. Mai haviem governat el nostre País, ningú dels nostres en tenia experiència, i sí governar un País no és tasca fàcil. Hem encertat en moltes coses i hem avançat en molts àmbits com mai s’havia fet, i també és cert que no hem arribat tan lluny com voldriem en alguns aspectes. També ens hem equivocat i ens hem tornat a alçar amb força aprenent de les errades per millorar. Del que també podeu estar ben segures i segurs és que cada dia d’estos huit anys en que m’he deixat la pell, he tingut sempre ben present l’horitzó cap on caminàvem col·lectivament i la importància de fer-ho amb mirada llarga i conviccions fermes.</p>

        <p>Ara, una dreta i una extrema dreta profundament reaccionàries campen desaforades per les nostres institucions i destrossen tot allò que troben al seu pas. Retallades, censura, coaccions... Al País Valencià des maig ho estem patint especialment, però també a Europa cada dia avancen més els intolerants. Hui, aquell horitzó europeu i mundial de pau, benestar i estabilitat amb què somiaven els nostres pares i mares queda enterbolit i sembla més lluny d’abastar que fa uns anys.</p>

        <p>Per això em presente al Parlament Europeu: perquè em negue a no fer tot el possible per capgirar aquesta situació. Ho faig amb la mateixa il·lusió que quan vaig voler capgirar l’educació, la cultura i l’esport valencians fa 8 anys, i amb més força, experència i energia que mai. Perquè cada dia que passa es fa més urgent la necessitat de plantar cara per a construir una nova Europa. Una nova Europa que pose fi a l'escalada bèl·lica, als discursos d'odi i a l'ascens de l'extrema dreta. Una nova Europa que protegisca els nostres drets lingüístics, els nostres llauradors i llauradores, les nostres indústries i els nostres sectors productius.</p>

        <p>Plantem cara per construir una nova Europa social que avance en drets per a la majoria treballadora i protegisca els drets humans ací i arreu del món. Una nova Europa que aposte per una transició energètica justa i que acabe amb l'especulació del nostre territori. Una Europa del pobles i de les nacions que supere l'actual club d'estats i l’Europa-mercat del capital i la competència deslleial ferotge. Una nova Europa on la cultura estiga present en tots els àmbits de les nostres vides i aposte pels i les seues professionals. Vull contribuir a bastir una nova Europa feminista que avance per la igualtat real i efectiva i combata totes les estructures heteropatriarcals del sistema. Una nova Europa més diversa, garant dels drets LGTBI i una nova Europa dels i les joves, que deixe de mirar amb displicència la nostra joventut i que en genere les condicions reals i efectives per a construir una vida digna i en llibertat, sense tuteles ni menyspreus.</p>

        <p>Per això, si m’ho permeteu, vull posar la meua experiència política, la meua capacitat de treball i el meu coneixement del País a disposició d’aquest gran repte. A Europa, treballaré incansablement per recórrer i representar cada racó del nostre País. I ho faré en coordinació amb els pobles i ciutats, amb el grup parlamentari de Les Corts, amb les nostres representants a les Diputacions i la Federació de Municipis i amb els nostres diputats i senador a Madrid.</p>

        <p>És el moment de plantar cara i donar un nou impuls a esta vella Europa. És el moment de transformar el nostre continent. Amb el teu suport, serem la veu valencianista, d’esquerres, feminista, ecologista i antifeixista a Europa. M’acompanyes?</p>
      </div>
    </div>
  </section>
</template>

<style scoped lang="scss">
.candidates {
  background: var(--orange);
  background-attachment: fixed;
  background-size: 150%;
  padding-top: 2rem;
  display: flex;
  flex-direction: column;
  justify-content: space-between;

  .container {
    width: 100%;
  }

  h2 {
    font-size: var(--text-3xl);
    color: var(--white);
  }

  &-description {
    color: var(--white);
    font-weight: bold;
    font-size: var(--text-md);
    margin-top: 3rem;
  }

  &-letter {
    background: var(--white);
    max-width: 800px;
    margin-block-start: 30vh;
    margin-block-end: var(--spacer-12);
    padding: var(--site-padding);

    p {
      font-size: var(--text-base);
      line-height: 1.5;
    }
  }
  
  .socials :deep(a) {
    color: var(--white);
    opacity: 1;
  }
}
</style>