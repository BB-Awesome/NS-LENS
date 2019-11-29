<template>
  <div>
    <div class="reis-omschrijving globaal">
      <div class="row-1">
        <div class="vertrek">
          <p>Utrecht Centraal</p>
        </div>
        <div class="connector">
          <p> - </p>
        </div>
        <div class="aankomst">
          <p>Den Haag Centraal</p>
        </div>
      </div>

      <div class="row-2">
        <div class="vertrek">
          <p>6:40</p>
        </div>
        <div class="connector">
          <p> - </p>
        </div>
        <div class="aankomst">
          <p>7:20</p>
        </div>
      </div>
    </div>

    <div class="reis-omschrijving stations lijst">
      <div class="treinrit-stop" v-for="stop in stops" v-bind:key="stop">
        <p style="display: none">{{stop}}</p>
        <TreinritStopComponent></TreinritStopComponent>
      </div>
    </div>
  </div>
</template>

<script>
// @ is an alias to /src
import TreinritStopComponent from '@/components/TreinritStopComponent.vue'

export default {
  name: 'home',
  components: {
    TreinritStopComponent
  },
  data() {
    return {
        stops: [1,2,3,4,5]
      }
  }
}
</script>

<style lang="scss">
  .reis-omschrijving.globaal .row-1, .reis-omschrijving.globaal .row-2 {
    display: flex;
    justify-content: center;
    padding: 10px;
    background-color: white;
    color: #003082;
    font-weight: bold;

    .connector p {
      margin-left: 5px;
      margin-right: 5px;
    }
  }

  .treinrit-stop {
    background-color: white;
  }
</style>
