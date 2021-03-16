<template>
  <div class="home page">
    <h1>This is Home Page!</h1>
    <p>
      Lorem ipsum dolor sit, amet consectetur adipisicing elit. Dignissimos iure
      perspiciatis unde odit soluta iusto mollitia voluptatibus sed eius rem,
      cumque totam atque facere. Eveniet sint delectus quam alias ratione
      placeat atque dignissimos explicabo possimus error ipsum, dolorum
      voluptatum accusamus, provident modi quaerat est. Error nulla consequatur
      et perferendis? Quaerat?
    </p>

    <button v-on:click="show = !show">
      {{ show == true ? this.animated : this.animate }}
    </button>
    <br /><br />
    <!-- v-on:click sama dengan @click -->

    <transition
      mode="in-out"
      enter-active-class="animate__animated animate__bounceInDown"
    >
      <img src="../assets/logo.png" v-if="show" />
    </transition>
  </div>
</template>

<script>
export default {
  name: "Home",
  data() {
    return {
      show: true,
      animated: "Animated!",
      animate: "Animate",
    };
  },
};
</script>
