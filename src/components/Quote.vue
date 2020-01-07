<template>
<div class="card rounded-0">
    <card
        img-direction="left"
        :img-src="characterImg"
        :img-alt="'image of ' + characterName"
        :class="{ 'shadow' : favorite }"
    >
        <p class="card-text">{{quote}}</p>
        <p class="card-text text-right font-italic">- {{characterName}}</p>
        <p class="card-text text-right">
            <button
                @click="updateFavorite(quoteId)"
                class="btn btn-default btn-sm"
                v-b-tooltip.hover
                title="like"
                style="font-size: 1.5rem;"
            >
                <span class="sr-only">like</span>
                <i v-if="!favorite" class="far fa-heart"></i>
                <i v-else class="fas fa-heart text-danger"></i>
            </button>
        </p>
    </card>
</div>
</template>

<script>
    import Card from './Card';

    export default {
      name: 'Quote',
      components: {
        Card
      },
      props: {
          characterImg: {
              type: String,
              default:
                  "https://en.wikipedia.org/wiki/Dunder_Mifflin#/media/File:Dunder_Mifflin,_Inc.svg"
          },
          characterName: {
              type: String,
              default: "Unknown Character"
          },
          quote: {
              type: String,
              default:
                  "Hello"
          },
          quoteId: Number,
          favorite: Boolean
      }
    }
</script>

<style lang="scss">

</style>
