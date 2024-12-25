
<script>
	import { onMount } from 'svelte';
    import '../app.css';
          // create a new hydra-synth instanc
     let width, height;
     let myCanvas; 
      onMount(() => {
        var hydra = new Hydra({ 
          detectAudio: false,
          })

        src(o0).layer(osc(5, 0.1, 0.1).colorama(0.99).luma(()=>Math.sin(time*0.9)*0.5))
          .modulate(shape(4).repeat(4,4).luma(), 2)
          .modulateRepeat(osc(10, 0.01).rotate(1), 0.6,4, 0.1, 0.01)
          .modulate(noise(0.8), 0.3)
          .out(o0);

          myCanvas = document.querySelector('canvas');
      });

      function handleResize() {
                myCanvas.width = width;
                myCanvas.height = height;
            // console.log(this.canvas)
          };
</script>

<main>
  <h1>softshadow</h1>
  <h2>live-looping saxophone and spoken word</h2>
  <ul>
    <li><a href="https://softshadow.bandcamp.com"><button>listen</button></a></li>
    <li><a href="https://www.youtube.com/@softshadowww"><button>watch</button></a></li>
    <li><a href="https://instagram.com/softshadow____"><button>follow</button></a></li>
    <li><a href="mailto:softshadowmusic@proton.me"><button>contact</button></a></li>
  </ul>
</main>

<style>

  main {
    background-color: rgba(0, 0, 0, 0.5);
    width: 100%;
    height: 100%;
    position: absolute;
    text-align: center;
  }

  h1, h2 {
    color: #C495FF;
   text-shadow: -6px 5px black;
  }

  h1 {
    font-size: 200px;
    font-family: 'Creepygirl';
    filter: blur(1px)

  }

  h2 {
    font-size: 15px;
    font-family: 'kidsplay';
  }
  
  ul {
    list-style-type: none;
    display: flex;
    flex-direction: column;
    width: 100%;
    padding: 0px;

  }

 li {
  margin-top: 30px;
 }




 button {
  background-color: rgba(56, 56, 56, 0.5);
  color: white;
  padding: 10px;
  border-radius: 5px;
  font-family: 'kidsplay';
  font-size: 20px;
  width: 200px;
  box-shadow: -6px 5px black;
 }

 @media (min-width:750px) {
    h1 {
      font-size: 100px;
    }

    h2 {
      font-size: 25px;
    }

    button {
      width: 300px;
      font-size: 25px;
    }
 }

</style>
