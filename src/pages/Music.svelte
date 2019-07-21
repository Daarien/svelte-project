<script>
  import AudioPlayer, { stopAll } from "../comp/AudioPlayer.svelte";
</script>

<button on:click={stopAll}>stop all audio</button>

<!-- https://musopen.org/music/9862-the-blue-danube-op-314/ -->
<AudioPlayer
  src="../assets/music/Моя земля.mp3"
  title="Моя земля"
  composer="Сколовы"
  performer="Сколовы" />

<!-- https://musopen.org/music/43775-the-planets-op-32/ -->
<AudioPlayer
  src="tutorial/music/holst.mp3"
  title="Mars, the Bringer of War"
  composer="Gustav Holst"
  performer="USAF Heritage of America Band" />

<!-- https://musopen.org/music/8010-3-gymnopedies/ -->
<AudioPlayer
  src="tutorial/music/satie.mp3"
  title="Gymnopédie no. 1"
  composer="Erik Satie"
  performer="Prodigal Procrastinator" />
