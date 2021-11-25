<script>
 import Timer from "./Timer.svelte";
 import HowTo from "./howTo.svelte";
 let audio;

 function timerEnds(e){
  audio.play();
 }

</script>

<style>
 h1, h3{
  text-align: center;
 }
</style>

<h1>Hand Washing App</h1>

<Timer on:end={timerEnds} />
<HowTo />
<h3>
 <a href="https://www.who.int/gpsc/clean_hands_protection/en/">Picture Source</a>

 <a href="https://freesound.org/people/metrostock99/sound/345086/">Sound Source</a>
</h3>

<audio bind:this={audio}>
 <source src="sound.mp3" />
</audio>