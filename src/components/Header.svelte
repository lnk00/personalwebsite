<style type="text/scss">
@import '../../public/assets/theme.scss';
@import '../../public/assets/container.scss';

.header {
  width: 100%;
  background-color: $dark;

  .right {
    @media (max-width: 1280px) {
      display: none;
    }
  }

  .left {
    @media (max-width: 480px) {
      transform: scale(0.6);
    }
  }

  .title-container {
    background-color: $green;
    padding: 6px 12px 6px 12px;
    display: inline-block;
    margin-bottom: 6px;
    margin-left: 6px;
    border-radius: 4px;

    h2 {
      font-weight: 400;
      font-size: 22px;
      margin: 0;
      color: $darker;
    }
  }

  h1 {
    line-height: 84px;
    font-size: 74px;
    margin: 0;
    color: $white;

    &.firstname {
      font-weight: 400;
    }
  }

  .works-container {
    cursor: pointer;
    display: flex;
    align-items: center;
    margin: 12px 0 0 6px;
  }

  h3 {
    margin: 0;
    font-weight: 400;
    color: $green;
  }

  .fa-arrow-circle-right {
    color: $green;
    margin-top: 4px;
    margin-left: 12px;
  }
}
</style>

<script>
import * as animateScroll from 'svelte-scrollto';
import Paralax from './Photo.svelte';
</script>

<div class="header">
  <div class="container">
    <div class="left">
      <div class="infos-container">
        <div class="title-container">
          <h2>Front-End Developer</h2>
        </div>
        <h1 class="firstname">DAMIEN</h1>
        <h1 class="lastname">DUMONTET</h1>
        <div
          class="works-container"
          on:click="{() => animateScroll.scrollTo({ element: '.exp' })}"
        >
          <h3>Get to know my works</h3>
          <i class="fas fa-arrow-circle-right"></i>
        </div>
      </div>
    </div>
    <div class="right">
      <Paralax />
    </div>
  </div>
</div>
