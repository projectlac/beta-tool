<template>
  <div class="Red px-4">
    <v-row>
      <div class="pickRed">
        <div>
          <div class="borderPickRed" v-for="(p, index) in pickRed" :key="index">
            <img :src="'./img/' + p.img" alt="" />
          </div>
        </div>
      </div>
      <div class="banRed">
        <div>
          <div class="borderBan" v-for="(b, index) in banRed" :key="index">
            <img :src="'./img/' + b.img" alt="" />
          </div>
        </div>
      </div>
      <div class="OmyRed" v-if="redOnmy.name">
        <img :src="'./img/' + redOnmy.img" alt="" />
      </div>
    </v-row>
  </div>
</template>

<script lang="ts">
import { Component, Prop, Vue } from "vue-property-decorator";

@Component({})
export default class Red extends Vue {
  @Prop() banRed!: Array<any>;
  @Prop() pickRed!: Array<any>;
  @Prop() redOnmy!: any;
}
</script>
