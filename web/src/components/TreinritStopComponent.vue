<template>
    <div class="treinrit-stop">
        <div class="vertrektijd"><p>12:27</p></div>
        <div class="lane"></div>
        <div class="right">
            <div class="station"><p>Utrecht Overvecht</p></div>
            <div class="platform"><p>8a</p></div>
        </div>
    </div>
</template>

<script lang="ts">
import { Component, Prop, Vue } from 'vue-property-decorator';

@Component
export default class TreinritStopComponent extends Vue {
  @Prop() private msg!: string;
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
    .treinrit-stop {
        display: flex;
        justify-content: space-between;
        padding: 20px;
        color: #003082;

        p {
            padding: 5px;
        }

        .vertrektijd, .station {
            font-weight: bold;
        }

        .right {
            width: 80vw;
            display: flex;
            justify-content: space-between;
            border-bottom: solid 1px #ececec;
        }
    }
</style>
