<template>
  <hooper :settings="hooperSettings">
    <slide v-for="(tesimonial, i) in testimonialContent" :key="i">
      <ul>
        <li class="item">
          <div class="texts">
            <p>
              {{ tesimonial.desc }}
            </p>
            <div class="author">
              <div class="image">
                <div
                  class="main"
                  :style="{ backgroundImage: 'url(' + tesimonial.imgSrc + ')' }"
                ></div>
              </div>
              <div class="short">
                <h3 class="author">
                  <span>{{ tesimonial.name }}</span>
                </h3>
                <h3 class="job">
                  <span>{{ tesimonial.designation }}</span>
                </h3>
              </div>
            </div>
          </div>
        </li>
      </ul>
    </slide>
  </hooper>
</template>

<script>
import { Hooper, Slide } from "hooper";
import "hooper/dist/hooper.css";
export default {
  components: {
    Hooper,
    Slide,
  },
  data() {
    return {
      testimonialContent: [
        {
          name: "Sónia Buvana,",
          designation: "Directora Geral",
          imgSrc: require("../../assets/img/about/1.jpg"),
          desc: `É uma jovem entusiasta
            moçambicana com experiência comprovada em Gestão
            de Recursos Humanos, Desenvolvimento do Capital
            Humano e Administração de Escritórios, actualmente a
            trabalhar como Consultora Independente. A paixão de
            Sonia está em "desbloquear o potencial" nas pessoas ao seu
            redor (em casa, no escritório, etc), tornando-a uma
            parceira perfeita para qualquer empresa que deseja atingir
            objetivos de médio a longo prazo por meio de pessoas
            engajadas e motivadas.`,
        },
        {
          name: "Watson Hamunakwadi",
          designation: "Especialista em Gestão Financeira",
          imgSrc: require("../../assets/img/about/2.jpg"),
          desc: `É actualmente o Director de Investimentos da Trans Industries e o Chefe do Grupo de Investimentos da Masawara Plc. 
          Ele supervisiona os investimentos, capital e crescimento do portfólio de empresas investidas pela Masawara em todo o portfólio 
          pan-africano investido em serviços financeiros, agroquímicos, hospitalidade, saúde, TIC, energia e propriedade. Watson tem 7 anos de experiência na 
          banca de investimento em finanças corporativas e comércio estruturado e financiamento de commodities e crédito para infraestruturas e recursos.`,
        },
        {
          name: "Vicente Matsinhe,",
          designation: "Especialista em Desenvolvimento do Sector Privado",
          imgSrc: require("../../assets/img/about/3.jpg"),
          desc: `Trabalhou como Coordenador Nacional de Projectos para um projecto financiado pelo GEF implementado pela UNIDO (Organização das Nações Unidas para 
          o Desenvolvimento Industrial), e muito recentemente aceitou o desafio de servir como Especialista Sênior em Desenvolvimento de Negócios, 
          num programa de Financiamento de Água, Saneamento e Higiene da USAID (WASH-FIN) implementado pela Tetra Tech ARD`,
        },
        {
          name: "Hélder Buvana,",
          designation: "Especialista em Digital Finance",
          imgSrc: require("../../assets/img/about/3.jpg"),
          desc: `É empresário e consultor apaixonado pelo Desenvolvimento Empresarial, Conteúdo Local, 
          Empresas Comunitárias, Fundos Sociais, Operações e Gestão da Cadeia de Suplemento, operando 
          entre Moçambique e a África do Sul. Hélder possui vasta experiência em Administração, Logística e Cadeia de 
          Abastecimento e trabalhou como Chefe de Operações - Lusófono na AMSCO e como Country Manager (Moçambique) para a NEPAD Business Foundation e Turner & Townsend`,
        },
      ],
      hooperSettings: {
        infiniteScroll: true,
        wheelControl: false,
        autoPlay: true,
        mouseDrag: false,
        transition: 600,
        playSpeed: 3500,
        itemsToShow: 1,
      },
    };
  },
};
</script>

<style lang="scss" scoped></style>
