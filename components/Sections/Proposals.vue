<script setup>
const proposals = {
  val: [
    {
      title: 'Pels interesos valencians',
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
  ],
  cas: [
    {
      title: 'Por los intereses valencianos',
      icon: 'IconsPV',
      color: 'orange',
      items: [
        'Desbloquearemos el <strong>Corredor Mediterráneo</strong>, infraestructura clave para la economía valenciana.',
        'Defenderemos unos <strong>precios justos para nuestro campo</strong> y protegeremos nuestros sectores productivos ante la competencia desleal de terceros países.',
        '<strong>Protegeremos nuestro territorio</strong> denunciando en Bruselas todos los macroproyectos especulativos como la ampliación del Puerto de València, el PAI de Llíber o la MAT en las comarcas de Castelló.',
        'Lucharemos para proteger la <strong>industria valenciana</strong> y exigiremos ayudas económicas para la descarbonización.'
      ]
    },
    {
      title: 'Para echar al gobierno de la vergüenza',
      icon: 'IconsDead',
      color: 'fuchsia',
      items: [
        'Mejoraremos la directiva europea de <strong>lucha contra la corrupción</strong>. No podemos permitir que el PP nos vuelva a robar.',
        'Propondremos una <strong>Ley Europea de Memoria Democrática</strong> frente aquellos que vuelen equiparar la dictadura con sus víctimas.',
        'Reclamaremos la <strong>oficialidad del valenciano</strong> en la Unión Europea y su pleno reconocimiento como una lengua europea que hay que promover y proteger.',
        'Blindaremos los <strong>servicios públicos</strong> (educación, sanidad, política social) en el pilar europeo de derechos sociales.'
      ]
    },
    {
      title: 'Por una nueva Europa',
      icon: 'IconsEurope',
      color: 'blue',
      items: [
        'Incorporaremos el delito de sexo no consentido y las <strong>violaciones como crímenes europeos</strong>.',
        'Blindaremos los <strong>derechos de las personas LGTBI+</strong> en toda la UE exigimos la implementación de la Estrategia para la Igualdad de las Personas LGTBI+ 2020-2025.',
        'Pediremos el <strong>reconocimiento del estado de Palestina</strong>, la suspensión del acuerdo de asociación de la Unión Europea con Israel y medidas para poner fin al genocidio palestino.',
        'Impulsaremos la <strong>jornada laboral de 32 horas</strong> en Europa.',
        'Reclamaremos una ley europea sobre el <strong>derecho a la vivienda</strong> que limite los precios del alquiler.'
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
  <section class="proposal" id="propostes" aria-labelledby="PropostesTitle">
    <h2 id="PropostesTitle" class="visually-hidden">{{ $t('proposals.title') }}</h2>
    <div
      v-for="category in proposals[$i18n.locale]"
      :key="category.icon"
      :class="[`color-${category.color}`, 'proposals']" 
    >
      <div class="container padded-x">
        <h3 class="proposal-title font-headline">
          <Component :is="icons[category.icon]" class="proposal-icon" />
          {{ category.title }}
        </h3>
      </div>
      <SiteSlider class="proposal-cards list-reset">
        <article v-for="proposal in category.items" :key="proposal" class="proposal-card">
          <p v-html="proposal" />
        </article>
      </SiteSlider>
    </div>
  </section>
</template>

<style lang="scss" scoped>
.proposal {
  padding-block-start: 1rem;

  &-title {
    display: flex;
    color: var(--blue);
    gap: var(--spacer-3);
    font-size: var(--text-xl);
    align-items: center;
    margin-top: var(--spacer-8);
    margin-bottom: -2rem;
  }

  &-icon {
    color: var(--color);
    height: 2.5em;
    width: 2.5rem;
    flex-shrink: 0;
  }

  &-cards {
    gap: var(--site-padding);
  }

  &-card {
    background: var(--color);
    color: var(--white);
    padding: var(--site-padding);
    font-size: var(--text-md);
    min-width: 40vw;
    min-height: 40vh;
    flex-shrink: 0;

    p {
      font-size: 1.1em;
    }

    strong {
      font-weight: 900;
    }
  }
}

@include media('<md') {
  .proposal {
    &-title {
      margin-bottom: 0;
    }

    &-card {
      width: 75vw;
      min-height: 25vh;
    }

    .slider {
      padding-inline: var(--site-padding);
    }
  }
}
</style>