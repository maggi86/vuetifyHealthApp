<template>
  <v-app :style="{background:$vuetify.theme.themes.light.background}">
    <v-layout row>
      <v-flex md8>
        <v-app :style="{background:$vuetify.theme.themes.dark.background}"
        class="rounded-tr-xl rounded-r-xl">
        <v-container>
          <v-col cols="12" sm="12">
            <v-app-bar color="white"
            flat
            class="mx-8 mb-8 mt-3">
            <v-text-field
            prepend-icon="mdi-magnify"
            color="purple"
            placeholder="Search your symptoms"
            flat>
          </v-text-field>
          <v-spacer></v-spacer>
          <v-chip class="ma-2" color="white">
            <v-icon left color="purple">
              mdi-clock-time-nine
            </v-icon>
            14:02 AM Today Nov,19
          </v-chip>
            </v-app-bar>
          </v-col>
          <v-col cols="12 mt-5" sm="12">
            <v-card class="mx-12 rounded-tl-xl rounded-bl-xl rounded-br-xl mt-n15">
              <v-list-item three-line>
                <v-list-item-content class="pa-10">
                  <v-list-item-title class="headline mb-1">
                    today <span class="purple--text">
                      -10%
                    </span> discount<br> on lung examinations
                  </v-list-item-title>
                  <v-list-item-subtitle>
                    this package price includes: consulation <br>
                    of a pilmonologist, spiroj, oijhj <span class="purple--text">></span>
                  </v-list-item-subtitle>
                </v-list-item-content>
                <v-list-item-avatar tile size="150" class="pr-10">
                  <img src="lungs.png">
                </v-list-item-avatar>
              </v-list-item>
            </v-card>
          </v-col>
          <v-col cols="12 mt-5" sm="12">
            <v-card class="mx-12 rounded-tl-xl rounded-tr-xl rounded-bl-xl rounded-br-xl mt-n10">
              <v-app-bar color="white" flat class="ma-8">
                <h5>
                  Statistics of your body
                </h5>
                <v-spacer></v-spacer>
          <v-btn color="purple" text>
            2019
            <v-icon right>
              mdi-chevron-down
            </v-icon>
            </v-btn>
            <v-btn color="purple" rounded dark depressed> Year
            </v-btn>
            <v-btn text>
              Month
            </v-btn>
          </v-app-bar>
          <template>
            <v-sparkline
            :value="value"
            color="purple"
            :smooth="radius || false"
            :padding="padding"
            :line-width="width"
            :stroke-linecap="lineCap"
            :fill="fill"
            :type="type"
            :auto-line-width="autoLineWidth"
            auto-draw
            >

            </v-sparkline>
          </template>
            </v-card>
          </v-col>
          <v-col cols="12" sm="12">
            <v-card class="mx-12 rounded-tl-xl rounded-tr-xl rounded-bl-xl rounded-br-xl mt-n4"
            color="purple">
            <v-list-item three-line>
                <v-list-item-content class="pa-2">
                    <v-list-item-title class="headline mb-1">
                      Heart rate <br>
                      <h2>112 bpm</h2>
                    </v-list-item-title> 
                </v-list-item-content>
                <v-list-item-avatar tile size="150" class="pr-10">
                  <v-icon size="100">fas fa-heartbeat</v-icon>
                </v-list-item-avatar>
              </v-list-item>
            </v-card>
          </v-col>
          <v-col cols="12" sm="6">
            <v-card class="mx-12 rounded-tl-xl rounded-tr-xl rounded-bl-xl rounded-br-xl mt-n12">
              <v-app-bar color="white" flat class="ma-8">
                <h5> Your Activity</h5>
                <v-spacer></v-spacer>
                <v-btn color="purple" rounded dark depressed>
                  Meals
                </v-btn>
                <v-btn text>
                  Month
                </v-btn>
              </v-app-bar>
            </v-card>
          </v-col>
        </v-container>
        </v-app>
      </v-flex>
      <v-flex md4>
        <v-app :style="{background:$vuetify.theme.themes.light.background}">
          <v-container>

          </v-container>
        </v-app>
      </v-flex>
    </v-layout>
  </v-app>
</template>

<script>
  export default{
   data:() => ({
    width:2,
    radius:100,
    padding:0,
    lineCap: 'round',
    value: [0,2,5,9,5,10,3,4,8,2,7,9,4,3,6],
    fill: false,
    type:'trend',
    autoLineWidth: false
   }),
   computed:{
    theme(){
      return this.$vuetify.theme.dark ? "dark" : "light";
    }
   }
  }
</script>
