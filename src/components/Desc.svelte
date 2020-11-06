<style type="text/scss">
@import '../../public/assets/theme.scss';

.desc {
  margin-top: 82px;
}

.title {
  color: $darker;
  font-size: 28px;
  background-color: $green;
  border-radius: 4px;
  padding: 8px;
  display: inline-block;
}

.subtitle {
  margin-top: 12px;
  color: $grey;
  font-size: 20px;
  font-style: italic;
}

.intro,
.feedback {
  margin-top: 24px;
  color: $dark-grey;
  font-size: 18px;
  line-height: 28px;
}

.tech-title {
  margin-top: 24px;
  font-size: 24px;
  color: $white;
}

.tech {
  display: flex;
  flex-wrap: wrap;
}

.tech-container {
  margin-top: 24px;
  margin-right: 24px;
  display: flex;
  align-items: center;
  justify-content: center;
  height: 75px;
  width: 75px;
  border-radius: 75px;
  background-color: $dark;

  .fa-angular {
    color: $angular;
    font-size: 40px;
  }

  .fa-node-js {
    color: $javascript;
    font-size: 40px;
  }

  .fa-css3-alt {
    color: $wordpress;
    font-size: 40px;
  }

  .fa-vuejs {
    color: $vue;
    font-size: 40px;
  }

  .fa-node-js {
    color: $javascript;
    font-size: 40px;
  }

  .fa-gem {
    color: $ruby;
    font-size: 34px;
  }

  .fa-wordpress {
    color: $wordpress;
    font-size: 40px;
  }

  .fa-node {
    color: $node;
    font-size: 40px;
  }
}
</style>

<script>
import { fly } from 'svelte/transition';
import { selectedCard } from '../store';

export let config;
</script>

{#key $selectedCard}
  <div
    class="desc"
    in:fly="{{ delay: 500, x: window.innerWidth / 2 }}"
    out:fly="{{ x: window.innerWidth / 2 }}"
  >
    <div class="title">{config.title}</div>
    <div class="subtitle">{config.subtitle}</div>
    <div class="intro">{config.intro}</div>
    <div class="tech-title">Technologies</div>
    <div class="tech">
      {#each config.techs as tech}
        <div class="tech-container {tech.label}">
          <i class="{tech.icon}"></i>
        </div>
      {/each}
    </div>
    <div class="feedback">{config.feedback}</div>
  </div>
{/key}
