<template>
  <div class="">
    <block
      animation="animation0"
      class="text-gray-50"
      :separator="true"
      title="L'auto-école qui en jette !"
      text="Lorem ipsum dolor sit amet, consectetur adipisicing elit. Molestiae, nemo. Natus minima voluptatem odio placeat debitis laboriosam consequatur nam error unde dolore. Exercitationem quasi molestias, maiores similique repellat qui minima!"
    >
      <img src="/svg/car1.svg" alt="" class="animated opacity-0">
    </block>
    <block
      animation="animation1"
      class="text-white"
      title-font-size="text-4xl"
      text-font-size="text-2xl"
      :svg-right="true"
      title="Code de la route"
      text="Lorem ipsum dolor sit amet consectetur adipisicing elit. Quidem quos mollitia nemo ex impedit dicta dolorum amet ullam, doloremque odio nesciunt consectetur incidunt perspiciatis alias, porro quas fuga. Neque, itaque?"
    >
      <img src="/svg/conceil1.svg" alt="" class="animated">
    </block>
    <block
      animation="animation2"
      class="text-green-50/50"
      title-font-size="text-4xl"
      text-font-size="text-2xl"
      title="Code de la route"
      text="Lorem ipsum dolor sit amet consectetur adipisicing elit. Quidem quos mollitia nemo ex impedit dicta dolorum amet ullam, doloremque odio nesciunt consectetur incidunt perspiciatis alias, porro quas fuga. Neque, itaque?"
    >
      <img src="/svg/car2.svg" class="animated opacity-0" alt="">
    </block>
    <div id="offres" class="flex flex-wrap my-48 justify-center content-between" comment="container mx-auto">
      <pricingBase
        prefix-emoji="🏍️"
        suffix-emoji="🛵"
        nom-offre="Permis Moto"
        prix="220€"
        :options="[
          'code moins de 20h ! 🙀 😏',
          'un autre truc'
        ]"
      />
      <pricingBase
        :popular="true"
        prefix-emoji="🚗"
        suffix-emoji="🚙"
        nom-offre="Permis B"
        prix="450€"
        :options="[
          'code 35h',
          'un autre truc',
          'encore un autre',
          'tout plein partout !'
        ]"
        info="Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum."
      />
      <pricingBase
        prefix-emoji="🚨"
        suffix-emoji="🚨"
        nom-offre="Stage de récupération de point"
        prix="80€"
        :options="[
          'Perdre des points, c\'est donner de l\'argent à l\'état et à Sab !',
          'Donc c\'est gentil !'
        ]"
        info="Faut pas perdre son permis de conduire 😞"
      />
    </div>
    <div id="l-equipes" class="py-48 flex flex-wrap mt-48 justify-center content-between bg-gray-50" comment="container mx-auto">
      <lEquipe
        :enseignants="[
          {nom:`PRUD'HOMME`, prenom:`Sabrina`, type:[`Monitrice`, `référente handicap`, `Chargée des relations avec les éléves`], autorisation: `A 02 042 0356 0`},
          {nom:`FOURNIER`, prenom:`Julien`, type:[`Moniteur`], autorisation: `A 03 042 0035 0`},
          {nom:`PRUD'HOMME`, prenom:`Jacques`, type:[`Moniteur`], autorisation: `A 08 042 0014 0`}]"
      />
    </div>
    <div id="maps" class="p-4 pb-24 flex flex-wrap justify-center content-between bg-gray-50" comment="container mx-auto" style="height: 850px">
      <maps class="w-2/3 shadow-inner overflow-hidden rounded-md" />
      <div class="w-1/3 shadow-lg" />
    </div>
  </div>
</template>

<script>
export default {
  name: 'IndexPage'
}
</script>
