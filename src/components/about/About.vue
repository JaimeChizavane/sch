<template>
  <div class="about_inner">
    <div class="left">
      <div class="image">
        <img src="../../assets/img/placeholders/1-1.jpg" alt="placeholder" />
        <div
          class="main"
          :style="{ backgroundImage: 'url(' + aboutImg + ')' }"
        ></div>
      </div>
      <!-- End image  -->
    </div>
    <!-- End left -->

    <div class="right">
      <div class="shane_tm_title">
        <span>Acerca</span>
        <h3>
          PERFIL DA EMPRESA
        </h3>
      </div>
      <div class="text">
        <p>
          SOLUÇÕES CAPITAL HUMANO (SCH) oferece apoio na fase inicial para aqueles empresários que procuram resolver 
          os problemas mais urgentes que afectam as comunidades de baixa renda ou desfavorecidas em Moçambique. 
          Produzir impacto social e económico e colaborar para o avanço dos Objetivos de Desenvolvimento Sustentável 
          (ODS) está no cerne da razão pela qual disponibilizamos nossos fundos.
        </p>
      </div>
      <div class="shane_tm_button">
        <a :href="cv" download>
          Saber mais
        </a>
      </div>
    </div>
    <!-- End right -->
  </div>
</template>

<script>
export default {
  data() {
    return {
      aboutImg: require("../../assets/img/about/4.jpg"),
      cv: require("../../assets/img/resume/resume.jpg"),
    };
  },
};
</script>
