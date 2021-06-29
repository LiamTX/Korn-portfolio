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
        <div>
          <v-card :loading="loading" class="mx-auto my-12" max-width="374">
            <template slot="progress">
              <v-progress-linear
                color="deep-purple"
                height="10"
                indeterminate
              ></v-progress-linear>
            </template>

            <v-img
              height="250"
              src="https://cdn.vuetifyjs.com/images/cards/cooking.png"
            ></v-img>

            <v-card-title>Cafe Badilico</v-card-title>

            <v-card-text>
              <v-row align="center" class="mx-0">
                <v-rating
                  :value="4.5"
                  color="amber"
                  dense
                  half-increments
                  readonly
                  size="14"
                ></v-rating>

                <div class="grey--text ms-4">4.5 (413)</div>
              </v-row>

              <div class="my-4 text-subtitle-1">$ • Italian, Cafe</div>

              <div>
                Small plates, salads & sandwiches - an intimate setting with 12
                indoor seats plus patio seating.
              </div>
            </v-card-text>

            <v-divider class="mx-4"></v-divider>

            <v-card-title>Tonight's availability</v-card-title>

            <v-card-text>
              <!-- <v-chip-group
              v-model="selection"
              active-class="deep-purple accent-4 white--text"
              column
            >
              <v-chip>5:30PM</v-chip>

              <v-chip>7:30PM</v-chip>

              <v-chip>8:00PM</v-chip>

              <v-chip>9:00PM</v-chip>
            </v-chip-group> -->
            </v-card-text>

            <v-card-actions> </v-card-actions>
          </v-card>
        </div>

        <div>
          <v-card :loading="loading" class="mx-auto my-12" max-width="374">
            <template slot="progress">
              <v-progress-linear
                color="deep-purple"
                height="10"
                indeterminate
              ></v-progress-linear>
            </template>

            <v-img
              height="250"
              src="https://cdn.vuetifyjs.com/images/cards/cooking.png"
            ></v-img>

            <v-card-title>Cafe Badilico</v-card-title>

            <v-card-text>
              <v-row align="center" class="mx-0">
                <v-rating
                  :value="4.5"
                  color="amber"
                  dense
                  half-increments
                  readonly
                  size="14"
                ></v-rating>

                <div class="grey--text ms-4">4.5 (413)</div>
              </v-row>

              <div class="my-4 text-subtitle-1">$ • Italian, Cafe</div>

              <div>
                Small plates, salads & sandwiches - an intimate setting with 12
                indoor seats plus patio seating.
              </div>
            </v-card-text>

            <v-divider class="mx-4"></v-divider>

            <v-card-title>Tonight's availability</v-card-title>

            <v-card-text>
              <!-- <v-chip-group
              v-model="selection"
              active-class="deep-purple accent-4 white--text"
              column
            >
              <v-chip>5:30PM</v-chip>

              <v-chip>7:30PM</v-chip>

              <v-chip>8:00PM</v-chip>

              <v-chip>9:00PM</v-chip>
            </v-chip-group> -->
            </v-card-text>

            <v-card-actions> </v-card-actions>
          </v-card>
        </div>

        <div>
          <v-card :loading="loading" class="mx-auto my-12" max-width="374">
            <template slot="progress">
              <v-progress-linear
                color="deep-purple"
                height="10"
                indeterminate
              ></v-progress-linear>
            </template>

            <v-img
              height="250"
              src="https://cdn.vuetifyjs.com/images/cards/cooking.png"
            ></v-img>

            <v-card-title>Cafe Badilico</v-card-title>

            <v-card-text>
              <v-row align="center" class="mx-0">
                <v-rating
                  :value="4.5"
                  color="amber"
                  dense
                  half-increments
                  readonly
                  size="14"
                ></v-rating>

                <div class="grey--text ms-4">4.5 (413)</div>
              </v-row>

              <div class="my-4 text-subtitle-1">$ • Italian, Cafe</div>

              <div>
                Small plates, salads & sandwiches - an intimate setting with 12
                indoor seats plus patio seating.
              </div>
            </v-card-text>

            <v-divider class="mx-4"></v-divider>

            <v-card-title>Tonight's availability</v-card-title>

            <v-card-text>
              <!-- <v-chip-group
              v-model="selection"
              active-class="deep-purple accent-4 white--text"
              column
            >
              <v-chip>5:30PM</v-chip>

              <v-chip>7:30PM</v-chip>

              <v-chip>8:00PM</v-chip>

              <v-chip>9:00PM</v-chip>
            </v-chip-group> -->
            </v-card-text>

            <v-card-actions> </v-card-actions>
          </v-card>
        </div>
      </div>
    </div>

    <div class="header"> 
      <p>Copyright © 2014 - 2021 ·Liam Cabral· Todos os Direitos Reservados</p>
    </div>
  </v-container>
</template>

<script>
export default {
  name: "Home",

  data: () => ({
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
    margin: 20px;
  }
}

.header {
  background-color: #1a1919;
  width: auto;
  color: white;
  text-align: center;
}
</style>
