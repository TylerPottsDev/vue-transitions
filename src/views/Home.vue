<template>
  <div class="home page">
    <h1>Home Page</h1>
    <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Adipisci facilis modi, blanditiis ea doloribus delectus id itaque aliquid quidem aspernatur praesentium fugiat repudiandae reprehenderit, odit provident reiciendis nulla harum inventore voluptas laudantium animi dolore error unde neque! Reiciendis, obcaecati doloribus!</p>
    <button @click="show = !show">ANIMATE</button>
    <transition name="img-anim">
      <div class="animate" v-show="show">
        <img src="@/assets/logo.png" width="150" />
      </div>
    </transition>
  </div>
</template>

<script>
export default {
  name: 'home',
  data () {
    return {
      show: false
    }
  }
}
</script>

<style>
.animate {
  margin: 25px 0px;
}
.img-anim-enter-active, .img-anim-leave-active {
  transition: transform 0.5s ease, opacity 0.5s ease;
}

.img-anim-enter, .img-anim-leave-to {
  transform: translateX(-100px) rotateZ(90deg);
  opacity: 0;
}

.anim-img-enter-to, .anim-img-leave {
  transform: translateX(0px) rotateZ(0deg);
  opacity: 1;
}
</style>

