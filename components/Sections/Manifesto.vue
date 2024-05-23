<template>
  <section class="manifesto" id="programa" aria-labelledby="ProgramaTitle">
    <div class="container padded manifesto-cols">
      <div>
        <div class="manifesto-sticky">
          <h2 id="ProgramaTitle" class="font-headline skew manifesto-title">
            <template v-if="$i18n.locale === 'val'">
              Programa<br>Eleccions<br>Europees<br>2024
            </template>
            <template v-else>
              Programa<br>Elecciones<br>Europeas<br>2024
            </template>
          </h2>
          <div class="manifesto-download">
            <p id="DownloadManifesto">{{ $t('manifesto.download') }}</p>
            <div class="flex">
              <a href="/docs/Programa_Eleccions_Europees_24_VAL.pdf" aria-describedby="DownloadManifesto">
                <Icon name="ri:download-line" />
                Valencià
              </a>
              <a href="/docs/Programa_Eleccions_Europees_24_CAS.pdf" aria-describedby="DownloadManifesto">
                <Icon name="ri:download-line" />
                Castellano
              </a>
            </div>
          </div>
        </div>
      </div>
      <div class="manifesto-cover" v-if="$i18n.locale === 'val'">
        <p>Després dels horrors del feixisme i de les guerres que van devastar el nostre continent, el projecte europeu va representar per a moltes generacions una llum d'esperança,  un far de pau, d’estabilitat i de benestar construït sobre els valors de la democràcia, la igualtat i la diversitat. Hui, aquella promesa d’una Europa unida, pròspera i segura sembla allunyar-se cada vegada més i més ràpid.</p>
        <p>Les guerres tornen a tocar a les portes d’Europa, l’extrema dreta cavalca desbocada l’onada d’odi que travessa el nostre continent, la crisi climàtica s’accelera i les desigualtats creixen cada dia. A allò que fins fa poc era excepcional hui li diem nova normalitat. </p>
        <p>Al País Valencià, la situació política no és gaire millor: PP i VOX campen lliures per les nostres institucions i destrueixen amb impunitat els consensos mínims del nostre autogovern. Censuren la nostra cultura, odien la nostra diversitat i ataquen els nostres serveis públics. Només busquen seguir enriquint-se i, mentrestant, ens divideixen.</p>
        <p>Aquestes eleccions són l’oportunitat per a l’esquerra valencianista de plantar cara. De plantar cara als dogmes neoliberals que empobreixen el nostre camp i la nostra indústria, però també de plantar cara a una dreta i extrema dreta que governa al nostre País i que amenaça amb governar també el nostre continent.</p>
        <p>Volem plantar cara a l’odi i l’extrema dreta. Volem plantar cara a les retallades i a l’austericidi. Volem plantar cara a la violència masclista, als règims totalitaris i als negacionistes climàtics. Volem plantar cara a tot aquell que vulga posar el País Valencià en el mapa internacional de la vergonya.</p>
        <p>Des de Compromís - Sumar, hem defensat sempre la necessitat de participar en la construcció del projecte europeu. D’una altra Europa, sí. D’una Europa que no deixe ningú enrere i que aposte decididament pels nostres interessos: com a ciutadans i ciutadanes d’un continent en transformació i com a poble valencià. </p>
        <p>El 9 de juny, plantem cara a Europa: pels interessos del nostre poble, per combatre el govern de PP i VOX i per construir una Europa social, democràtica, verda, feminista i justa. Una Europa al servei de les persones i que plante cara a les amenaces amb valentia. Perquè nosaltres no ens resignem. Nosaltres, amb tu, plantem cara. Ara, també a Europa.</p>
      
        <a href="/docs/Programa_Eleccions_Europees_24_VAL.pdf">
          <Icon name="icons8:document" />
          Continúa llegint...
          <span>PDF</span>
        </a>
      </div>
      <div v-else class="manifesto-cover">
        <p>Después de los horrores del fascismo y de las guerras que devastaron nuestro continente, el proyecto europeo representó para muchas generaciones una luz de esperanza, un faro de paz, de estabilidad y de bienestar construido sobre los valores de la democracia, la igualdad y la diversidad. Hoy, aquella promesa de una Europa unida, próspera y segura parece alejarse cada vez más y más rápido.</p>
        <p>Las guerras vuelven a tocar a las puertas de Europa, la extrema derecha cabalga desbocada la oleada de odio que atraviesa nuestro continente, la crisis climática se acelera y las desigualdades crecen cada día. A aquello que hasta hace poco era excepcional hoy le decimos nueva normalidad.</p>
        <p>En el País Valenciano, la situación política no es muy mejor: PP y VOX campan libras por nuestras instituciones y destruyen con impunidad los consensos mínimos de nuestro autogobierno. Censuran nuestra cultura, odian nuestra diversidad y atacan nuestros servicios públicos. Solo buscan seguir enriqueciéndose y, mientras tanto, nos dividen.</p>
        <p>Estas elecciones son la oportunidad para la izquierda valencianista de hacer frente. De hacer frente a los dogmas neoliberales que empobrecen nuestro campo y nuestra industria, pero también de hacer frente a una derecha y extrema derecha que gobierna en nuestro País y que amenaza con gobernar también nuestro continente.</p>
        <p>Queremos hacer frente al odio y la extrema derecha. Queremos hacer frente a los recortes y al austericidi. Queremos hacer frente a la violencia machista, a los regímenes totalitarios y a los negacionistas climáticos. Queremos hacer frente a todo aquel que quiera poner el País Valenciano en el mapa internacional de la vergüenza.</p>
        <p>Desde Compromís - Sumar, hemos defendido siempre la necesidad de participar en la construcción del proyecto europeo. De otra Europa, sí. De una Europa que no dejo nadie atrás y que apuesto decididamente por nuestros intereses: como ciudadanos y ciudadanas de un continente en transformación y como pueblo valenciano.</p>
        <p>El 9 de junio, hacemos frente a Europa: por los intereses de nuestro pueblo, para combatir el gobierno de PP y VOX y para construir una Europa social, democrática, verde, feminista y justa. Una Europa al servicio de las personas y que hago frente a las amenazas con valentía. Porque nosotros no nos resignamos. Nosotros, contigo, hacemos frente. Ahora, también a Europa.</p>
      
        <a href="/docs/Programa_Eleccions_Europees_24_CAS.pdf">
          <Icon name="icons8:document" />
          Continuar leyendo...
          <span>PDF</span>
        </a>

      </div>
    </div>
  </section>
</template>

<style lang="scss" scoped>
.manifesto {
  background: var(--fuchsia);
  color: var(--white);
  padding-block: 4rem;

  &-sticky {
    position: sticky;
    top: 5rem;
  }

  h2 {
    font-size: var(--text-3xl);
    line-height: 1;
  }

  &-cols {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: var(--site-padding);
  }

  &-cover {
    background: var(--white);
    padding: var(--site-padding);
    font-size: var(--text-base);
    line-height: 1.25;
    color: var(--blue);

    a {
      display: flex;
      padding: 1em 1.5em;
      text-decoration: none;
      background: var(--orange);
      color: var(--white);
      font-weight: bold;
      align-items: center;
      gap: 1em;
      border: 3px var(--orange) solid;

      &:hover {
        background: var(--white);
        color: var(--orange);
      }

      span {
        margin-inline-start: auto;
      }
    }
  }

  &-download {
    margin-block-start: 4rem;
    font-size: var(--text-md);

    p {
      font-weight: 900;
    }

    a {
      display: inline-flex;
      color: var(--fuchsia);
      background: var(--white);
      text-decoration: none;
      font-weight: 900;
      align-items: center;
      gap: var(--spacer-2);
      padding: .5em;
    }

    .flex {
      display: flex;
      gap: var(--spacer-4);
    }
  }
}

@include media('<md') {
  .manifesto {
    &-cols {
      grid-template-columns: 1fr;
    }
  }
}
</style>