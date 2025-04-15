<script setup>
import { ref } from "vue";

const newsletter = ref([ 
{
  id: 1,
  cover: "https://s2-g1.glbimg.com/azBLZntp1jcRpWEP_BqWsEDuGAE=/0x0:4096x2732/984x0/smart/filters:strip_icc()/i.s3.glbimg.com/v1/AUTH_59edd422c0c84a879bd37670ae4f538a/internal_photos/bs/2025/H/r/6PvF0BSdGSsbSp4WGObQ/goybjjkx0aal0oc.jpg",
  title: "Katy Perry no espaço: Blue Origin completa voo com 6 mulheres a bordo",
  date: "14/04/2025",  
  font: "https://g1globo.com" ,
  address: "https://g1.globo.com/inovacao/noticia/2025/04/14/katy-perry-no-espaco-lancamento-blue-origin.ghtml" ,
  subject: "A Blue Origin lançou com sucesso, na manhã desta segunda-feira (14), a nave New Shepard para uma viagem de turismo espacial com 6 mulheres a bordo. Entre elas, estavam a cantora Katy Perry e a jornalista Lauren Sánchez — noiva do bilionário Jeff Bezos, que é o dono da empresa de foguetes.O lançamento ocorreu às 10h31 (de Brasília), e tanto a cápsula quanto o foguete retornaram em segurança cerca de dez minutos depois. O g1 transmitiu a viagem ao vivo.",

},
{
  id: 2,
  cover: "https://s2-g1.glbimg.com/6tqLTgQUu5fdm9r-7bXX8IfmIUU=/0x0:5255x3504/984x0/smart/filters:strip_icc()/i.s3.glbimg.com/v1/AUTH_59edd422c0c84a879bd37670ae4f538a/internal_photos/bs/2025/y/i/y9giiTT3CHS5A167Annw/2025-04-14t224442z-162525619-rc2kwdaoqtsj-rtrmadp-3-usa-trump-universities.jpg",
  title: "Harvard se nega a cumprir exigências de Trump, e governo congela mais de US$ 2 bilhões em recursos",
  date: "14/04/2025",  
  font: "https://g1globo.com" ,
  address: "https://g1.globo.com/mundo/noticia/2025/04/14/governo-trump-congela-cerca-de-us-23-bilhoes-em-financiamento-para-harvard.ghtml" ,
  subject: "O governo dos Estados Unidos anunciou nesta segunda-feira (14) o congelamento de cerca de US$ 2,3 bilhões (R$ 13,1 bilhões) em subsídios e contratos com a Universidade de Harvard. Mais cedo, a instituição disse que não vai cumprir exigências da gestão de Donald Trump, como o fim de programas de inclusão e equidade. ",
},
{
  id: 3,
  cover: "https://s2-g1.glbimg.com/Q5lRkk6NiWkJK0mBF-gwmaKxnzc=/0x0:1839x931/984x0/smart/filters:strip_icc()/i.s3.glbimg.com/v1/AUTH_59edd422c0c84a879bd37670ae4f538a/internal_photos/bs/2025/8/z/vBSAVESwiaWG2saAkMUQ/trump.jpg",
  title: "Trump, Beyoncé, Jay-Z, DiCaprio, Will Smith: as festas milionárias de Diddy frequentadas por celebridades ",
  date: "15/04/2025",  
  font: "https://g1globo.com" ,
  address: "https://g1.globo.com/fantastico/noticia/2025/04/15/trump-beyonce-jay-z-dicaprio-will-smith-as-festas-milionarias-de-diddy-frequentadas-por-celebridades.ghtml" ,
  subject: "Magnata da música e símbolo do rap dos anos 1990, Sean Combs, também conhecido como Puff Daddy ou P. Diddy, viu o seu império desmoronar em um dos maiores escândalos da indústria do entretenimento. O rapper está preso desde 2024 e o seu julgamento está marcado para 5 de maio. Se condenado, pode pegar prisão perpétua.",
},
]);
</script>

<template>
 <section>
  <h1>Portal da Becker</h1>
  <article class="news">
    <ul>
      <li v-for="(news , id) in newsletter" :key="id">
        <h2>{{ news.title }}</h2>
        <img :src="news.cover" alt="capa">
        <p>{{ news.subject }}</p>
        <div>
          <p>Fonte: <a href="news.font">{{ news.font }}</a></p>
          <p>Link: <a href="news.address">{{ news.address }}</a></p>
        </div>
      </li>
    </ul>
  </article>
 </section>
</template>

<style scoped>
section {
  max-width: 1200px;
  margin: 2rem auto;
  padding: 1rem;
  font-family: "Arial", sans-serif;
}

h1 {
  text-align: center;
  font-size: 2.5rem;
  color: #1e1e1e;
  margin-bottom: 2.5rem;
  text-transform: uppercase;
  letter-spacing: 1px;
  font-weight: bold;
  border-bottom: 4px solid #1e88e5;
  display: inline-block;
  padding-bottom: 0.5rem;
}

.news ul {
  list-style: none;
  padding: 0;
  margin: 0;
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
  gap: 1.5rem;
}

.news li {
  background-color: #ffffff;
  border-radius: 10px;
  box-shadow: 0 2px 8px rgba(0, 0, 0, 0.07);
  overflow: hidden;
  display: flex;
  flex-direction: column;
  transition: transform 0.3s ease;
}

.news li:hover {
  transform: scale(1.02);
}

.news img {
  width: 100%;
  height: 160px;
  object-fit: cover;
}

.news h2 {
  font-size: 1.1rem;
  margin: 0.8rem;
  color: #333;
  height: 3.3em;
  overflow: hidden;
}

.news p {
  margin: 0.5rem 0.8rem;
  color: #555;
  font-size: 0.9rem;
  line-height: 1.4;
  height: 4.2em; 
  overflow: hidden;
}

.news div {
  margin: 0.8rem;
  font-size: 0.8rem;
  color: #777;
}

.news a {
  color: #1e88e5;
  text-decoration: none;
  word-break: break-all;
}

.news a:hover {
  text-decoration: underline;
}
</style>
