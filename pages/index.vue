<template>
  <div>
        <canvas id="unity-canvas"   style=" background: red ;width: 800px; height:600px" ></canvas>

  </div>
</template>
<script>

export default {
  mounted(){
      console.log("ok")
    createUnityInstance(document.querySelector("#unity-canvas"), {
        dataUrl: "/game/Build/game.data",
        frameworkUrl: "/game/Build/game.framework.js",
        codeUrl: "/game/Build/game.wasm",
        streamingAssetsUrl: "StreamingAssets",
        companyName: "DefaultCompany",
        productName: "MiniFighterHome",
        productVersion: "0.1",
        //matchWebGLToCanvasSize: false, // Uncomment this to separately control WebGL canvas render size and DOM element size.
         devicePixelRatio: 1, // Uncomment this to override low DPI rendering on high DPI displays.
      });
  }
}
</script>