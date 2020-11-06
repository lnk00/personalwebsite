<style type="text/scss">
@import '../../public/assets/theme.scss';

.card {
  cursor: pointer;
  width: 100%;
  background-color: $dark;
  border-radius: 4px;
  padding: 32px;
  box-sizing: border-box;
  display: flex;
  align-items: center;
  margin-bottom: 24px;
  transition: all 1s;

  &.active {
    transform: scale(1.1);
  }

  .left {
    margin-right: auto;
    .title {
      font-weight: 900;
      font-size: 20px;
      color: $white;
    }

    .subtitle {
      font-weight: 200;
      font-size: 14px;
      color: $grey;
      font-style: italic;
    }
  }

  .fa-vuejs {
    color: $vue;
    font-size: 42px;
  }

  .fa-angular {
    color: $angular;
    font-size: 42px;
  }

  .fa-gem {
    color: $ruby;
    font-size: 36px;
  }

  .fa-wordpress {
    color: $wordpress;
    font-size: 42px;
  }
}
</style>

<script>
import { selectedCard } from '../store';
export let icon;
export let title;
</script>

<div class="card" class:active="{title === $selectedCard}" on:click>
  <div class="left">
    <slot />
    <div class="title">
      <slot name="title">Slot needed</slot>
    </div>
    <div class="subtitle">
      <slot name="subtitle">Slot needed</slot>
    </div>
  </div>
  <div class="right"><i class="{icon}"></i></div>
</div>
