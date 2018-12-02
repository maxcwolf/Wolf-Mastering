<template>
  <div class="home">
    <v-parallax dark :src="require('../assets/studio-knobs-md.jpg')">
      <v-layout align-center column justify-center>
        <h1 class="display-3 font-weight-bold mb-3">Wolf Mastering</h1>
        <h4 class="subheading">
          A custom mastering studio offering the finest in digital and analog
          sonic treatment since 1996
        </h4>
      </v-layout>
    </v-parallax>
    <img alt="Vue logo" src="../assets/wolf-logo.webp" />
    <HelloWorld msg="Wolf Mastering" />
    <p>
      WOLF Mastering, a mastering studio located on Nashville's Music Row,
      provides mastering services for all recording genres and clients
      throughout the world. Mastering engineer Erik Wolf, owner and operator of
      Wolf Mastering, learned his craft in Los Angeles, then worked for the
      legendary Bernie Grundman Mastering in Hollywood, California for five
      years before moving to Nashville to start his own mastering studio in
      1996.
    </p>
    <div class="ricksum" id="ricksum">
      <p>
        Mind your own goddamn business, Gene! I'm having a conversation with my
        mother here! Kissing Rick's ass isn't gonna make him stay, Mom, but it
        will help you lose everyone else. Okay, take it easy Rick. T-that's
        dark. What about the reality where Hitler cured cancer, Morty? The
        answer is: Don't think about it. God-damn!
      </p>
      <p>
        Nobody's killing me until after I catch my wife with another man. No
        jumping in the sewer! Man, that guy is the Red Grin Grumbold of
        pretending he knows what's going on. Oh you agree huh? You like that Red
        Grin Grumbold reference? Well guess what, I made him up. You really are
        your father's children. Think for yourselves, don't be sheep. Then let
        me GET to know you!
      </p>
      <p>
        I am Mr. Booby Buyer. I'll buy those boobies for 25 schmeckles! Well I
        don't like your unemployed genes in my grandchildren, Jerry. Wow I
        really crononberg'd up the whole place huh Morty, just a bunch a
        cronenbergs walkin around. You know my name, that's disarming.
      </p>
      <p>
        No jumping in the sewer! If it were, you could call ME Ernest Hemingway.
        Alien Invasion Tomato Monster Mexican Armada Brothers Who Are Just
        Regular Brothers Running In A Van From An Asteroid And All Sorts Of
        Things: The Movie. Like nothing shady ever happened in a fully furnished
        office? You ever hear about Wall Street Morty? You know what those guys
        do in their fancy board rooms? They take their balls and dip 'em in
        cocaine and wipe 'em all over each other. You know Grandpa goes around
        and he does his business in public because grandpa isn't shady.
      </p>
      <p>
        I'm Mr. Crowbar, and here is my friend, who is also a crowbar! Nice, Mrs
        Pancakes. Real nice. Aww, gee, you got me there, Rick. Hi! Principal
        Vagina: the name's real, possibly Scandinavian.
      </p>
      <p>
        Nothing to read into there! I'm a bit of a stickler Meeseeks, what about
        your short game? Are you invisible and you're gonna, like, fart on me?
        It's like the N word and the C word had a baby, and it was raised by all
        the bad words for Jews.
      </p>
    </div>
  </div>
</template>

<script>
// @ is an alias to /src
import HelloWorld from "@/components/HelloWorld";

export default {
  name: "home",
  components: {
    HelloWorld
  }
};
</script>
