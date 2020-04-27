<template functional>
    <div class="scene">
        <div class="card">
            <div class="card__face card__face--front">
                <img :src="props.item.imgSrc">
            </div>
            <div class="card__face card__face--back">{{props.item.content}}</div>
        </div>
    </div>
</template>

<script>
export default {
  name: 'FlipItem',
  props: ['item'],
}
</script>

<style>
.scene {
  width: 200px;
  height: 260px;
  perspective: 600px;
}

.card {
  width: 100%;
  height: 100%;
  position: relative;
  transition: transform 1s;
  transform-style: preserve-3d;
  transition-delay: calc( 2s + (0.3s * var(--i)));
}

.card__face {
  position: absolute;
  height: 100%;
  width: 100%;
  backface-visibility: hidden;
  display: flex;
  align-items: center;
  justify-content: center;
}

.card__face--front {
  background: #6889FF;
}

.card__face--back {
  background: #000;
  color: #fff;
  transform: rotateY( 180deg );
}

.flip-enter .card {
  transform: rotateY(180deg);
}
</style>
