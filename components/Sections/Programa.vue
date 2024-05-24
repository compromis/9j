<script setup>
const proposals = {
  val: [
    {
      title: 'Pels interessos valencians',
      icon: 'IconsPV',
      color: 'orange',
      items: [
        'Desbloquejarem el <strong>Corredor Mediterrani</strong>, infraestructura clau per a l’economia valenciana.',
        'Defensarem uns <strong>preus justos per al nostre camp</strong> i protegirem els nostres sectors productius davant de la competència deslleial de tercers països.',
        '<strong>Protegirem el nostre territori</strong> denunciant a Brussel·les tots els macroprojectes especulatius com l’ampliació del Port de València, PAI de Llíber o la MAT a les comarques de Castelló.',
        'Lluitarem per protegir la <strong>indústria valenciana</strong> i exigirem ajudes econòmiques per a la descarbonització.'
      ]
    },
    {
      title: 'Per fer fora al govern de la vergonya',
      icon: 'IconsDead',
      color: 'fuchsia',
      items: [
        'Millorarem la directiva europea de lluita <strong>contra la corrupció</strong>. No podem permetre que el PP ens torne a robar.        .',
        'Proposarem una <strong>Llei Europea de Memòria Democràtica</strong> front aquells que volen equiparar la dictadura amb les seues víctimes.',
        'Reclamarem l’<strong>oficialitat del valencià a la Unió Europea</strong> i el seu ple reconeixement com una llengua europea que cal promoure i protegir.',
        'Blindarem els <strong>serveis públics</strong> (educació, sanitat, política social) en el pilar europeu de drets socials.'
      ]
    },
    {
      title: 'Per una nova Europa',
      icon: 'IconsEurope',
      color: 'blue',
      items: [
        'Incorporarem el delicte de sexe no consentit i les violacions com a <strong>crims europeus.</strong>',
        'Blindarem els <strong>drets de les persones LGTBI+</strong> en tota la UE exigint la implementació de l\'Estratègia per a la Igualtat de les Persones LGTBI+ 2020-2025.',
        'Demanarem el <strong>reconeixement de l’estat de Palestina</strong>, la suspensió de l’acord d’associació de la Unió Europea amb Israel i mesures per posar fi al genocidi palestí.',
        'Impulsarem la <strong>jornada laboral de 32 hores</strong> a Europa.',
        'Reclamarem una llei europea sobre el <strong>dret a l’habitatge</strong> que limite els preus del lloguer.'
      ]
    }
  ]
}

const icons = {
  IconsPV: resolveComponent('IconsPV'),
  IconsDead: resolveComponent('IconsDead'),
  IconsEurope: resolveComponent('IconsEurope')
}
</script>

<template>
  <section class="proposals" id="propostes" aria-labelledby="PropostesTitle">
    <h2 id="PropostesTitle" class="visually-hidden">{{ $t('proposals.title') }}</h2>
    <div class="container padded">
      <div
        v-for="category in proposals[$i18n.locale]"
        :key="category.icon"
        :class="[`color-${category.color}`, 'proposals-card']" 
      >
        <h3 class="proposals-title font-headline">
          <Component :is="icons[category.icon]" class="proposals-icon" />
          {{ category.title }}
        </h3>
        <ol>
          <li v-for="proposal in category.items" :key="proposal" class="proposals-item">
            <p v-html="proposal" />
          </li>
        </ol>
      </div>
    </div>
  </section>
</template>

<style lang="scss" scoped>
.proposals {  
  .container {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: var(--site-padding);
  }

  &-title {
    display: flex;
    color: var(--blue);
    gap: var(--spacer-3);
    font-size: var(--text-xl);
    align-items: center;
    margin: 0;
    line-height: 1;
  }

  &-icon {
    color: var(--color);
    height: 2.5rem;
    width: 2.5rem;
    flex-shrink: 0;
  }

  &-card {
    background: var(--light-gray);
    padding: var(--site-padding);

    ol {
      margin: 0;
      padding: 0;
    }

    li {
      border-bottom: 1px var(--blue) solid;
      list-style: none;
      font-size: var(--text-base);
      line-height: 1.25;
      padding: 1rem 0;
    }
  }
}
</style>