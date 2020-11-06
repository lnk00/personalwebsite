<style type="text/scss">
@import '../../public/assets/theme.scss';
@import '../../public/assets/container.scss';

.exp {
  background-color: $darker;
  width: 100%;
  overflow: hidden;

  @media (min-width: 980px) {
    max-height: 814px;
  }

  .container {
    align-items: flex-start;
  }

  .left {
    flex-direction: column;
    align-items: flex-start;
    padding-right: 48px;

    @media (max-width: 980px) {
      display: none;
    }

    .title {
      color: $white;
      font-size: 28px;
      font-weight: 900;
      margin-bottom: 48px;
    }

    .card-container {
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: center;
      width: 100%;
    }
  }

  .right {
    flex-direction: column;
    align-items: flex-start;
    justify-content: flex-start;
    padding-left: 48px;

    @media (max-width: 980px) {
      padding-left: 0;
    }

    .desc-container {
      @media (max-width: 980px) {
        display: none;
      }
    }

    .desc-responsive-container {
      @media (min-width: 980px) {
        display: none;
      }
    }
  }
}
</style>

<script>
import Card from './Card.svelte';
import Desc from './Desc.svelte';
import configService from '../config.service';
import { selectedCard } from '../store';

let onClickCard = (card) => {
  selectedCard.set(card.title);
};
</script>

<div class="exp">
  <div class="container">
    <div class="left">
      <div class="title">Experiences</div>
      <div class="card-container">
        {#each configService.card as card}
          <Card
            icon="{card.icon}"
            title="{card.title}"
            on:click="{onClickCard.bind(this, card)}"
          >
            <span slot="title">{card.title}</span>
            <span slot="subtitle">{card.subtitle}</span>
          </Card>
        {/each}
      </div>
    </div>
    <div class="right">
      <div class="desc-container">
        <Desc
          config="{configService.desc.find((e) => e.title === $selectedCard)}"
        />
      </div>
      <div class="desc-responsive-container">
        <Desc config="{configService.desc[0]}" />
        <Desc config="{configService.desc[1]}" />
        <Desc config="{configService.desc[2]}" />
        <Desc config="{configService.desc[3]}" />
      </div>
    </div>
  </div>
</div>
