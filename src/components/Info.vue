<template>
  <div class="info-container">
    <div class="info-sec">
      <div class="data-key">Realm</div>
      <div>
        {{guildData.realm}}
        <span class="divider">|</span>
        {{guildData.faction}}
      </div>
    </div>
    <div class="info-sec">
      <div class="data-key">Progress</div>
      <div>
        <div class="progress-list" v-for="(value, name) in guildData.progress" :key="name">
          {{name}}
          <span class="divider">|</span>
          {{value}}
        </div>
      </div>
    </div>
    <div class="info-sec">
      <div class="data-key">Recruiting</div>
      <div class="class-container">
        <span
          class="rowdata"
          v-for="classname in guildData.recruiting"
          :key="classname"
          v-bind:class="classname"
        >{{classname}}</span>
      </div>
    </div>
    <div class="info-sec">
      <div class="data-key">Contact Info</div>
      <div>
        <span class="rowdata" v-for="detail in guildData.contact" :key="detail">{{detail}}</span>
      </div>
    </div>
  </div>
</template>
<style lang="scss">
.progress-list {
  text-transform: capitalize;
}
.divider {
  color: red;
}
</style>
<script>
import guildData from "@/data/data.js";
export default {
  data() {
    return {
      guildData
    };
  },
  created() {
    
  }
};
</script>
