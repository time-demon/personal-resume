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

  >.introCon {
    padding: 0 10px 0 30px;

    >.projectBox {
      >.projectTitle {
        display: flex;
        vertical-align: top;
        justify-content: space-between;
        line-height: 18px;
        padding: 0 0 5px;


        >.projectTitleRight {
          font-size: 13px;
          width: 125px;
          text-align: right;

          >a {
            padding: 0 2px;
          }

          >span {
            padding: 0 5px 0 5px;
            color: #ccc;
          }
        }
      }
    }
  }
}

.keyW1 {
  background: #f6f6f6;
  padding: 2px 5px;
  border-radius: 5px;
  border: 1px solid #eee;
  margin: 0 2px;
}
</style>