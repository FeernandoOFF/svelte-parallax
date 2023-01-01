<script>
  import { Parallax, ParallaxLayer } from 'svelte-parallax';
</script>

<div class="sticky top-0 bg-red-300 w-screen h-[10vh] z-20" />
<div class="bg-gray-200">
  <Parallax sections={3}>
    <ParallaxLayer offset={0.25} span={2} rate={0.3}>
      <h1 class="text-5xl text-center">
        Hey, I'm
        <br />
        Fernando Obregon
      </h1>
    </ParallaxLayer>
    <ParallaxLayer rate={-2}>
      <b
        class="text-[400px] text-center opacity-30 absolute top-[-100px] left-[50%] translate-x-[-50%] "
        >OFF</b
      ></ParallaxLayer
    >
    <ParallaxLayer offset={0.75}>
      <div
        class="w-[80vw] h-full mx-auto  border-t-2 border-gray-500 bg-blue-100"
      >
        I'm changing the background color!
      </div>
    </ParallaxLayer>

    <ParallaxLayer
      offset={1}
      rate={-2.5}
      style="display: flex; justify-content: flex-end;"
    >
      <div
        style="background-color: lightblue; opacity: 0.5; width: 50%; height: 100%;"
      />
    </ParallaxLayer>

    <ParallaxLayer
      offset={1}
      rate={2.5}
      style="display: flex; justify-content: flex-start;"
    >
      <div
        style="background-color: yellow; opacity: 0.5; width: 50%; height: 100%;"
      />
    </ParallaxLayer>
  </Parallax>
</div>
