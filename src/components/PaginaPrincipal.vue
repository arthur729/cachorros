<template>
  <body>
    <i>
      <h1>Site de cachorro</h1>
    </i>
    <h2>Para ver os melhores cachorros do Brasil</h2>
    <ImagensInterativas/>
    <Tabela />
    <VideoDisciplina/>
  </body>
</template>

<script>

import Tabela from "./TabelaPessoas.vue";
import ImagensInterativas from "./ImagensInterativas.vue";
import VideoDisciplina from "./VideoDisciplina.vue";

export default {
  name: 'PaginaPrincipal',
  props: {
        msg: String
    },
  components: {
    Tabela, ImagensInterativas, VideoDisciplina,
}
};
</script>

<style>
/* Estilos gerais */
.flex-container {
  display: flex;
  flex-direction: column;
  align-items: center;
  text-align: center;
  margin: 20px auto;
}

.img-container {
  margin-bottom: 20px;
}

.img-group {
  display: flex;
  flex-wrap: wrap;
  gap: 20px; /* Espaço entre as imagens */
  justify-content: center;
}

.cachorro-img {
  width: 100%;
  max-width: 250px; /* Largura máxima */
  height: auto;
  border-radius: 15px;
  transition: transform 0.3s, box-shadow 0.3s;
}

.cachorro-img:hover {
  transform: scale(1.05);
  box-shadow: 0 0 10px rgba(0, 0, 0, 0.2);
}

/* Estilos da tabela */
.table-container {
  width: 100%;
  overflow-x: auto;
  margin: 20px auto;
}

table {
  width: 100%;
  border-collapse: collapse;
  background-color: #fff;
  border: 1px solid #ddd;
}

th,
td {
  padding: 12px;
  text-align: left;
  border-bottom: 1px solid #ddd;
}

th {
  background-color: #f2f2f2;
}

.tabela-img {
  width: 100px;
  height: 100px;
  object-fit: cover;
  border-radius: 10px;
  transition: transform 0.3s, box-shadow 0.3s;
}

.tabela-img:hover {
  transform: scale(1.05);
  box-shadow: 0 0 10px rgba(0, 0, 0, 0.2);
}

/* Estilos do iframe */
.espaçamento {
  text-align: center;
}

iframe {
  width: 100%;
  max-width: 853px;
  height: auto;
  border: none;
  border-radius: 10px;
}

/* Responsividade */
@media (max-width: 600px) {
  .tabela-img {
    width: 80px;
    height: 80px;
  }

  th,
  td {
    display: block;
    width: 100%;
    box-sizing: border-box;
  }

  th {
    position: absolute;
    top: -9999px;
    left: -9999px;
  }

  td {
    border: none;
    position: relative;
    padding-left: 50%;
    text-align: right;
  }

  td:before {
    content: attr(data-label);
    position: absolute;
    left: 0;
    width: 50%;
    padding-left: 10px;
    font-weight: bold;
    text-align: left;
    white-space: nowrap;
  }
}

@media (max-width: 900px) {
  .img-group {
    flex-direction: column;
    gap: 10px;
  }
}


.video-container {
  position: relative;
  padding-bottom: 70%; /* Proporção 16:9 */
  height: 0;
  overflow: hidden;
  max-width: 100%;
  border-radius: 10px; /* Bordas arredondadas, se desejado */
  margin: 20px auto; /* Centraliza o vídeo */
}


</style>