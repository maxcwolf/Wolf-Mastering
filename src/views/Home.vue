<template>
  <div class="home">
    <v-parallax dark :src="require('../assets/studio-knobs-md.jpg')">
      <v-layout align-center column justify-center>
        <h1 class="display-4 font-weight-bold mb-3 para-heading">
          Wolf Mastering
        </h1>
        <h4 class="title font-italic">
          A custom mastering studio offering the finest in digital and analog
          sonic treatment since 1996
        </h4>
      </v-layout>
    </v-parallax>
    <v-layout
      justify-space-around
      fill-height
      pa-4
      class="main main-raised elevation-24"
    >
      <v-flex>
        <v-card> <v-img></v-img> </v-card>
      </v-flex>
      <v-flex ma-4>
        <v-card pa-4>
          <v-img :src="require('@/assets/erik.webp')"></v-img>
          <p>
            Erik Wolf- "I've been mastering for many years, long enough to see
            many changes. When I started, I cut lacquers which were used to
            press vinyl records. That required a unique set of skills. Getting a
            recording to fit on one side of a record, one groove, from lead in
            to lead out, requires finesse and experience. When the industry
            changed, I learned early CD mastering on the Sony PCM 1630 with the
            most current technology at the time. Later, digital work stations
            were incorporated into the mastering. Though there have been
            changes, the process and the skills are basically the same.The role
            of the mastering engineer requires a combination of artistic and
            technical skills. Providing an objective set of ears and
            understanding to get the most from each recording. This will result
            in a great sounding project, one that will sound great on all types
            of playback. Big speakers or earbuds, CDs and MP3s."
          </p>
        </v-card>
      </v-flex>
      <v-flex ma-2>
        <v-card pa-2>
          <div class="ricksum" id="ricksum">
            <p>
              WOLF Mastering, a mastering studio located on Nashville's Music
              Row, provides mastering services for all recording genres and
              clients throughout the world. Mastering engineer Erik Wolf, owner
              and operator of Wolf Mastering, learned his craft in Los Angeles,
              then worked for the legendary Bernie Grundman Mastering in
              Hollywood, California for five years before moving to Nashville to
              start his own mastering studio in 1996.
            </p>
          </div>
        </v-card>
      </v-flex>
    </v-layout>
  </div>
</template>

<script>
export default {
  name: "home"
};
</script>

<style>
.para-heading {
  font-family: "Audiowide" !important;
}
/* font-family: 'Audiowide', cursive;
font-family: 'Aldrich', sans-serif;
font-family: 'Rammetto One', cursive; */

.main {
  background: #ffffff;
  position: relative;
  z-index: 3;
}

.main-raised {
  margin: -40px 40px 0px;
  border-radius: 6px;
}
</style>
