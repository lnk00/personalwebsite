<style type="text/scss">
@import '../../public/assets/theme.scss';

.photo-container {
  position: relative;
  display: flex;
  align-items: center;
  justify-content: center;
  width: 700px;
  height: 700px;

  .img-container {
    border-radius: 500px;
    height: 500px;
    width: 500px;
    position: relative;
    background-color: $darker;
    display: inline-block;
    overflow: hidden;
  }

  .tech-container {
    position: absolute;
    display: flex;
    align-items: center;
    justify-content: center;
    background-color: $darker;
    height: 100px;
    width: 100px;
    border-radius: 100px;
    box-shadow: -19px 15px 50px -8px rgba(0, 0, 0, 0.5);
    transform: scale(0);
    animation: 1s cubic-bezier(0.645, 0.045, 0.355, 1) scaleup;
    animation-fill-mode: forwards;

    &.angular {
      top: 100px;
      left: 100px;
      height: 110px;
      width: 110px;
      border-radius: 110px;
      animation-delay: 200ms;

      .fa-angular {
        color: $angular;
        font-size: 55px;
      }
    }

    &.vue {
      height: 140px;
      width: 140px;
      border-radius: 140px;
      top: 205px;
      right: 40px;

      .fa-vuejs {
        color: $vue;
        font-size: 70px;
      }
    }

    &.node {
      height: 120px;
      width: 120px;
      border-radius: 120px;
      bottom: 75px;
      right: 140px;
      animation-delay: 300ms;

      .fa-node {
        color: $node;
        font-size: 60px;
      }
    }

    &.js {
      top: 100px;
      right: 140px;
      animation-delay: 500ms;

      .fa-node-js {
        color: $javascript;
        font-size: 50px;
      }
    }

    &.css {
      bottom: 80px;
      left: 120px;
      height: 140px;
      width: 140px;
      border-radius: 140px;
      animation-delay: 600ms;

      .fa-css3-alt {
        color: $wordpress;
        font-size: 70px;
      }
    }
  }

  .light-particule {
    background-color: $green;
    height: 10px;
    width: 10px;
    border-radius: 10px;
    position: absolute;
    bottom: 200px;
    right: 60px;
    transform: scale(0);
    animation: 1s cubic-bezier(0.645, 0.045, 0.355, 1) scaleup;
    animation-fill-mode: forwards;
    animation-delay: 800ms;
  }

  .dark-particule {
    background-color: $darker;
    height: 50px;
    width: 50px;
    border-radius: 60px;
    position: absolute;
    top: 100px;
    right: 80px;
    transform: scale(0);
    animation: 1s cubic-bezier(0.645, 0.045, 0.355, 1) scaleup;
    animation-fill-mode: forwards;
    animation-delay: 700ms;

    &.second {
      top: 640px;
      left: 250px;
    }
  }
}

@keyframes scaleup {
  from {
    transform: scale(0);
  }
  to {
    transform: scale(1);
  }
}
</style>

<script>
</script>

<div class="photo-container">
  <div class="img-container">
    <img src="assets/portait.png" alt="portrait" />
  </div>
  <div class="tech-container angular"><i class="fab fa-angular"></i></div>
  <div class="tech-container vue"><i class="fab fa-vuejs"></i></div>
  <div class="tech-container node"><i class="fab fa-node"></i></div>
  <div class="tech-container js"><i class="fab fa-node-js"></i></div>
  <div class="tech-container css"><i class="fab fa-css3-alt"></i></div>
  <div class="dark-particule"></div>
  <div class="dark-particule second"></div>
  <div class="light-particule"></div>
</div>
