<template>
  <canvas
    ref="matrixCanvas"
    class="fixed top-0 left-0 w-full h-full z-0 pointer-events-none bg-black"
  ></canvas>
</template>

<script setup>
import { onMounted, onUnmounted, ref } from 'vue';

const matrixCanvas = ref(null);
let interval = null;

onMounted(() => {
  const canvas = matrixCanvas.value;
  const ctx = canvas.getContext('2d');

  const characters = "0123456789ABCDEFGHIJKLMNOPQRSTUVWXYZｦｱｳｴｵｶｷｹｺｻｼｽｾｿﾀﾁﾂﾃﾄﾅﾆﾇﾈﾉﾊﾋﾌﾍﾎﾏﾐﾑﾒﾓﾔﾕﾖﾗﾘﾙﾚﾛﾜﾝ日ht月火水木金土上下左右前後";
  const fontSize = 16;

  let columns = 0;
  let drops = [];

  const initMatrix = () => {
    // ZMĚNA: Vždy bereme jen výšku viditelného okna
    canvas.width = window.innerWidth;
    canvas.height = window.innerHeight;

    columns = Math.floor(canvas.width / fontSize);
    drops = Array(columns).fill(1);
  };

  const draw = () => {
    ctx.fillStyle = 'rgba(0, 0, 0, 0.1)';
    ctx.fillRect(0, 0, canvas.width, canvas.height);

    // ZMĚNA: Přidán 'bold' a o něco vyšší opacita (0.35) pro ostřejší vzhled
    ctx.fillStyle = 'rgba(0, 245, 255, 0.35)';
    ctx.font = `bold ${fontSize}px monospace`;

    for (let i = 0; i < drops.length; i++) {
      const text = characters.charAt(Math.floor(Math.random() * characters.length));
      ctx.fillText(text, i * fontSize, drops[i] * fontSize);

      if (drops[i] * fontSize > canvas.height && Math.random() > 0.975) {
        drops[i] = 0;
      }
      drops[i]++;
    }
  };

  initMatrix();
  window.addEventListener('resize', initMatrix);
  interval = setInterval(draw, 50);

  onUnmounted(() => {
    clearInterval(interval);
    window.removeEventListener('resize', initMatrix);
  });
});
</script>
