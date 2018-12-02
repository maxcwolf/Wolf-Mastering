<template>
  <div class="home">
    <v-container fluid pa-0 grid-list-md>
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
      <v-layout fill-height row pa-4 class="main main-raised elevation-24">
        <v-flex ma-2 mt-4 xs8>
          <!-- <div class="main title-raised center">
          <h3 class="card-title">About Erik Wolf</h3>
          </div>-->
          <v-card pa-3 class="card-under elevation-10">
            <v-layout row class="flex-under">
              <v-flex xs6>
                <v-responsive>
                  <v-img :src="require('@/assets/erik.webp')"></v-img>
                </v-responsive>
              </v-flex>
              <v-flex xs6>
                <v-card-text class="subheading font-italic">
                  <i class="fas fa-quote-left"></i> I've been mastering for many
                  years, long enough to see many changes. When I started, I cut
                  lacquers which were used to press vinyl records. That required
                  a unique set of skills. Getting a recording to fit on one side
                  of a record, one groove, from lead in to lead out, requires
                  finesse and experience. When the industry changed, I learned
                  early CD mastering on the Sony PCM 1630 with the most current
                  technology at the time. Later, digital work stations were
                  incorporated into the mastering. Though there have been
                  changes, the process and the skills are basically the same.The
                  role of the mastering engineer requires a combination of
                  artistic and technical skills. Providing an objective set of
                  ears and understanding to get the most from each recording.
                  This will result in a great sounding project, one that will
                  sound great on all types of playback. Big speakers or earbuds,
                  CDs and MP3s. <i class="fas fa-quote-right"></i> <br />- Erik
                  Wolf
                </v-card-text>
              </v-flex>
            </v-layout>
          </v-card>
        </v-flex>
        <v-flex ma-2 xs4>
          <v-card pa-2 class="elevation-10">
            <div>
              <v-card-title class="card-title">About</v-card-title>
              <v-card-text py-0 class="subheading">
                WOLF Mastering, a mastering studio located on Nashville's Music
                Row, provides mastering services for all recording genres and
                clients throughout the world. Mastering engineer Erik Wolf,
                owner and operator of Wolf Mastering, learned his craft in Los
                Angeles, then worked for the legendary Bernie Grundman Mastering
                in Hollywood, California for five years before moving to
                Nashville to start his own mastering studio in 1996.
              </v-card-text>
              <v-card-text py-0 class="subheading"
                >Each recording is different and requires its own sonic
                treatment. The best and only way you can hear the difference
                after mastering is to hear a sample of your own recording
                mastered by WOLF Mastering. Upon request, WOLF Mastering is
                happy to offer a free sample mastering of your recording. This
                is not just the "run it through plug-ins, louder is better"
                approach.</v-card-text
              >
            </div>
          </v-card>
        </v-flex>
      </v-layout>
      <v-layout>
        <v-flex>
          <v-card>
            <iframe
              width="470"
              height="265"
              src="https://www.youtube.com/embed/8sbgT6m_gCg"
              frameborder="0"
              allow="accelerometer; encrypted-media; gyroscope; picture-in-picture"
              allowfullscreen
            ></iframe>
          </v-card>
        </v-flex>
      </v-layout>
    </v-container>
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
}

.main-raised {
  margin: -40px 40px 0px !important;
  border-radius: 6px;
  position: relative;
  z-index: 3 !important;
}

.title-raised {
  margin: -40px 75px 15px !important;
  border-radius: 3px;
  padding: 10px 0;
  background: linear-gradient(60deg, #6692bb, #aa924f);
  z-index: 15 !important;
}

.card-under {
  margin: -20px 0 !important;
}

.flex-under {
  margin: -10px 0 !important;
}

.card-title {
  font-size: 28px;
  font-family: "Audiowide" !important;
}
</style>
