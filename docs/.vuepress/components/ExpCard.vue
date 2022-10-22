<template>
  <div class="md-exp-card" :class="{ 'show-border': !hideBorder}">
    <div v-if="image" class="exp-card-image">
      <img :src="$withBase(image)" alt="">
    </div>
    <div class="exp-card-content">
      <slot></slot>
    </div>
  </div>
</template>

<script>
export default {
  props: ['image', 'hideBorder']
};
</script>

<style lang="stylus">
@import './styles/config.styl';

.md-exp-card
  background-color $frontColor
  margin-top 1em
  min-height 50px
  display grid
  grid: auto-flow dense / 240px 400px 1fr;
  flex-direction row
  align-items: center
  .exp-card-image
    display flex
    align-items center
    padding 0.5rem
    img 
      max-width 220px
      max-height 50px
      weight 100%
      height 50px
      border: 0px solid #eee;
      border-radius 0.2rem
      object-fit contain
  .exp-card-content
    padding 1rem
    flex-grow 1
    align-items center
    p
      line-height normal
      -webkit-margin-before 0em
      -webkit-margin-after 0.5em
    blockquote 
      font-size 1rem

.md-exp-card.show-border
  border 1px solid #eee
  border-radius 0.5rem
  box-shadow 0 5px 15px -5px rgba(0,0,0,.1)
  padding 0.5rem

@media (max-width: $MQMobileNarrow)
  .md-exp-card
    display flex
    flex-direction column
    margin 1rem -0.5rem
    padding 0.5rem
    box-sizing border-box
    .exp-card-image
      flex-grow 1
      align-items: stretch
      img 
        width 100%
        max-width 400px
    .exp-card-content
      pre
        margin 0
        border-radius 6px

</style>