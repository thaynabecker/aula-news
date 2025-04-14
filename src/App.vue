<script setup>
const noticias = [ {
  id: 1,
  titulo: 'Katy Perry no espaço: Blue Origin completa voo com 6 mulheres a bordo ',
  description: 'A Blue Origin lançou com sucesso, na manhã desta segunda-feira (14), a nave New Shepard para uma viagem de turismo espacial com 6 mulheres a bordo. Entre elas, estavam a cantora Katy Perry e a jornalista Lauren Sánchez — noiva do bilionário Jeff Bezos, que é o dono da empresa de foguetes.O lançamento ocorreu às 10h31 (de Brasília), e tanto a cápsula quanto o foguete retornaram em segurança cerca de dez minutos depois. O g1 transmitiu a viagem ao vivo.'
},
{
  id: 2,
  name: 'Item 2',
  details: { description: 'Item 2 description', price: 20.0 },
},
{
  id: 3,
  name: 'Item 3',
  details: { description: 'Item 3 description', price: 30.0 },
},
];
</script>

<template>
 <section>
  <h1>Notícias</h1>
  <article>
  {{ noticias }}
  </article>
 </section>
</template>

<style scoped>

</style>
