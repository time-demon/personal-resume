<template>
  <div class="myIntroBox">
    <div class="myIntroBox_left">
      <skill />
      <expProj />
    </div>
    <div class="myIntroBox_right">
      <openProj />
    </div>
  </div>
</template>

<script>
import skill from "@/components/intros/skill.vue";
import openProj from "@/components/intros/openProj.vue";
import expProj from "@/components/intros/expProj.vue";
export default {
  components: {
    skill,
    openProj,
    expProj,
  },
};
</script>

<style lang="scss">
.bold {
  font-weight: bold;
  font-size: 15px;
}

.introBox {
  padding: 20px 20px 10px;
}

.keyW1 {
  background: #f6f6f6;
  padding: 2px 5px;
  border-radius: 5px;
  border: 1px solid #eee;
  margin: 0 5px;
}
</style>