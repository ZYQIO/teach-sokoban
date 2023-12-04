<template>
  <div>
    <div v-for="(row, i) in map" class="flex">
      <div v-for="(col, j) in map[i]">
        <template v-if="map[i][j] === MapTitle.WALL">
          <img :src="wallImg" alt="" />
        </template>
        <template v-if="map[i][j] === MapTitle.FLOOR">
          <img :src="floorImg" alt="" />
        </template>
      </div>
    </div>
  </div>
</template>
  
  <script setup lang="ts">
import floorImg from "./../../assets/floor.png";
import wallImg from "./../../assets/wall.png";
import { useMapStore, MapTitle } from "../../store/map";

const { map } = useMapStore();
</script>
  
  <style scoped>
</style>
  