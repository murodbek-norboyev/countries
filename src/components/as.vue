<template>
<v-row>
      <v-col cols="6">
        <v-img
          :src="countryData.flag"
          :alt="countryData.name"/>
      </v-col>
      <v-col cols="6">
        <div class="mt-8">
          <h2>{{ countryData.name }}</h2>
          <v-row class="mt-3">
            <v-col lg="12" md="12" sm="12" xs="12">
              <div
                :class="`d-flex justify-space-between flex-wrap`"
                style="height: 100%"
              >
                <div>
                  <div>
                    <b>Native Name: </b
                    >{{ countryData.nativeName }}
                  </div>
                  <div>
                    <b>Population: </b
                    >{{ countryData.population | showDecimalPoint }}
                  </div>
                  <div><b>Region: </b>{{ countryData.region }}</div>
                  <div><b>Sub Region: </b>{{ countryData.subregion }}</div>
                  <div><b>Capital: </b>{{ countryData.capital }}</div>
                </div>
                <div>
                  <div>
                    <b>Top Level Domain: </b
                    ><span
                    class="mr-2"
                  >{{ countryData.topLevelDomain[0] }} </span
                  >
                  </div>
                  <div>
                    <b>Currencies: </b><span
                    class="mr-2"
                  > {{ currencies }}</span
                  >
                  </div>
                  <div>
                    <b>Languages: </b
                    ><span
                    class="mr-2"
                  >{{ languages }}
                    </span>
                  </div>
                </div>
              </div>
            </v-col>
          </v-row>
          <div class="mt-2">
            Border Countries:
            <span>
              <v-btn
                class="mr-2 mb-2"
                v-for="(bc, i) in borderCountries"
                :key="i"
              >{{ bc }}</v-btn
              >
            </span>
          </div>
        </div>
      </v-col>
    </v-row>
</template>

<script>
export default {
  name: 'as'
}
</script>

<style scoped>

</style>
