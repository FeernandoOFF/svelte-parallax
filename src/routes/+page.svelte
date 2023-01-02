<script>
  import { Parallax, ParallaxLayer, StickyLayer } from 'svelte-parallax';
</script>

<div class="sticky top-0 bg-red-300 w-screen h-[10vh] z-20" />
<div class="bg-gray-200">
  <Parallax sections={4}>
    <!-- Titles -->
    <ParallaxLayer offset={0.25} span={2} rate={0.3}>
      <h1 class="text-5xl text-center">
        Hey, I'm
        <br />
        Fernando Obregon
      </h1>
    </ParallaxLayer>
    <ParallaxLayer rate={2} let:progress>
      <div class="mx-auto w-full text-center">
        <b
          class="text-[400px] text-center opacity-30 "
          style="transform: scale({(progress > 0.2 ? progress : 0.5) * 100}%);"
          >OFF
        </b>
      </div>
    </ParallaxLayer>
    <!-- Text line -->
    <ParallaxLayer offset={0.75}>
      <div
        class="w-[80vw] h-full mx-auto  border-t-2 border-gray-500 bg-blue-100"
      >
        I'm changing the background color!
      </div>
    </ParallaxLayer>

    <!-- Yellow layer -->
    <StickyLayer offset={{ top: 1.2, bottom: 2 }} let:progress>
      <div class="flex relative h-full transition-all">
        <div
          style="background-color: yellow; opacity: 0.5; width: 50%; height: 100%;"
          class="transition-all  absolute {progress > 0.5
            ? 'right-0'
            : 'left-0'} grid place-items-center"
        >
          <p
            style="transform:scale({(progress > 0.6 ? progress : 0.6) * 200}%)"
          >
            I'm getting bigger
          </p>
          <h2>{progress}</h2>
        </div>
      </div>
    </StickyLayer>
    <!-- Half layers -->
    <ParallaxLayer
      offset={1}
      rate={2.5}
      style="display: flex; justify-content: flex-end;"
    >
      <div
        style="background-color: lightblue; opacity: 0.5; width: 50%; height: 100%;"
      />
    </ParallaxLayer>
    <!-- Green layer -->
    <ParallaxLayer
      offset={2}
      rate={2.5}
      style="display: flex; justify-content: flex-start;"
    >
      <div class="w-1/2 bg-green-600 h-full" />
    </ParallaxLayer>
    <ParallaxLayer offset={3.5} rate={2.5}>
      <h2 class="text-[200px] text-center opacity-30 ">That's it!</h2>
    </ParallaxLayer>
  </Parallax>
</div>
