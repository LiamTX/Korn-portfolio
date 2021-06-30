<template>
  <v-container>
    <div>
      <v-toolbar class="toolbar" color="grey darken-4">
        <v-toolbar-title class="toolbar-title">KORN</v-toolbar-title>
        <v-toolbar-item class="toolbar-item"
          ><a href="">Nossa jornada</a></v-toolbar-item
        >
        <v-toolbar-item class="toolbar-item"
          ><a href="">Albuns</a></v-toolbar-item
        >
      </v-toolbar>
    </div>

    <div class="carousel">
      <v-carousel>
        <v-carousel-item
          v-for="(item, i) in items"
          :key="i"
          :src="item.src"
          reverse-transition="fade-transition"
          transition="fade-transition"
        ></v-carousel-item>
      </v-carousel>
    </div>

    <div class="about">
      <div>
        <p>
          Formado em 1990, em Bakersfield, Korn vendeu 40 milhões de discos
          desde seu primeiro album(korn) em 1994, o que faz com que seja uma das
          bandas de metal mais bem sucedidas das ultimas decadas.
        </p>

        <p>
          Até o momento, Korn teve 7 nomeações para o Grammy Awards, tendo ganho
          2 vezes.
        </p>
      </div>
    </div>

    <div class="albuns">
      <div class="albuns-div">
        <div v-for="album_info of albuns_info" :key="album_info.title">
          <album-card :data="album_info" />
        </div>
      </div>
    </div>

    <div class="header">
      <p>Copyright © 2014 - 2021 ·Liam Cabral· Todos os Direitos Reservados</p>
    </div>
  </v-container>
</template>

<script>
import AlbumCard from "../components/AlbumCard.vue";
import img_links from "../utils/img-links";

export default {
  name: "Home",

  components: {
    AlbumCard,
  },

  data: () => ({
    albuns_info: [
      {
        img: img_links.the_leader,
        title: "The Leader",
        about:
          "Follow the Leader é o terceiro álbum de estúdio da banda estaduniense de Nu Metal Korn. O álbum foi lançado em 18 de agosto de 1998, pelo selo Immortal/Epic. Este foi o primeiro álbum da banda a não ser produzido por Ross Robinson, mas por Steve Thompson e Toby Wright. O álbum chegou à primeira colocação em quatro paradas, incluindo a Billboard 200 com 268 mil unidades vendidas apenas na primeira semana após o lançamento. Follow The Leader é considerado pelos membros do Korn como o álbum de maior sucesso comercial, sendo certificado cinco vezes como platina pela RIAA. Seus singles 'Got The Life' e 'Freak on a Leash' estrelaram em mais de três paradas, e seus clipes são considerados os primeiros a serem 'aposentados' da MTV, mais notavelmente no programa Total Request Live da mesma emissora.",
      },
      {
        img: img_links.issues,
        title: "Issues",
        about:
          "Issues é o quarto álbum de estúdio da banda de nu metal Korn, lançado a 16 de Novembro de 1999. O álbum chegou imediatamente ao primeiro lugar no topo de vendas. Desde seu lançamento, o álbum já vendeu mais de 13 milhões de cópias em todo o mundo. Falling Away From Me foi nomeado para os VMA de 2000 na categoria de Melhor Videoclipe de Rock. O Korn foi considerado o 53º Melhor artista de Hard Rock de sempre, pela VH1. Issues foi um sucesso comercial, estreando em primeiro lugar na Billboard 200 , com 575,000 unidades vendidas em sua primeira semana de lançamento. Em 22 de dezembro de 1999 Issues foi certificado 3x platina em os EUA Com 3.450.000 de cópias vendidas. Em 2020, a revista Metal Hammer o elegeu como um dos 20 melhores álbuns de metal de 1999.",
      },
      {
        img: img_links.the_nothing,
        title: "The Nothing",
        about:
          "The Nothing é o décimo terceiro álbum de estúdio da banda de nu metal Korn, lançado em 13 de setembro de 2019. Foi produzido por Nick Raskulinecz. O portal Loudwire o elegeu como um dos 50 melhores discos de metal de 2019.",
      },
    ],

    model: 0,
    items: [
      {
        src: "https://i1.wp.com/www.wikimetal.com.br/wp-content/uploads/2021/04/Korn.jpg?resize=1170%2C658&ssl=1",
      },
      {
        src: "https://i0.wp.com/guitarload.com.br/wp-content/uploads/2020/12/korn-1995-guitarra-de-7-cordas-1.jpg?fit=800%2C419&ssl=1",
      },
      {
        src: "https://images.vice.com/noisey/content-images/article/jonathan-davis-avalia-os-11-discos-do-korn/korn.jpg?crop=0.9253819036427732xw:1xh;center,center",
      },
      {
        src: "https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQZRRou0kM0MvHGPNbBFWVpdeZsQRMID91WEw&usqp=CAU",
      },
    ],
  }),
};
</script>

<style lang="scss">
* {
  font-family: "Arapey", serif;
}

.container {
  max-width: 100% !important;
  margin: 0 !important;
  padding: 0 !important;
}

.toolbar {
  .toolbar-title {
    font-size: 50px !important;
    color: white;
  }

  .toolbar-item {
    margin-left: 50px;
    font-size: 25px;
  }

  .toolbar-item a {
    text-decoration: none;
  }
}

.about {
  background-color: rgb(201, 195, 195);
  margin: 30px;
  font-size: 37px;
}

.about div {
  margin: 10px;
}

.albuns {
  background-color: #212121;

  .albuns-div {
    display: flex;
    flex-direction: row;
    justify-content: space-between;
    // margin: 20px;
    margin-left: 20px;
    margin-top: 20px;
    margin-right: 20px;

    p {
      font-size: 17px;
      color: black;
    }
  }
}

.header {
  display: flex;
  justify-content: center;
  background-color: #1a1919;
  width: auto;
  color: white;
  align-items: center;
  text-align: center;
  height: 70px;

  p {
    font-size: 20px;
  }
}
</style>
