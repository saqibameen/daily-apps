<template>
  <da-modal class="go-modal" @close="$emit('close')">
    <div class="go-modal__graphics">
      <da-svg src="/graphics/arrow.svg" class="go-modal__arrow left first"/>
      <da-svg src="/graphics/arrow.svg" class="go-modal__arrow left second"/>
      <da-svg src="/graphics/arrow.svg" class="go-modal__arrow left third"/>
      <da-svg src="/graphics/barcode.svg" class="go-modal__barcode"/>
      <da-svg src="/graphics/arrow.svg" class="go-modal__arrow third"/>
      <da-svg src="/graphics/arrow.svg" class="go-modal__arrow second"/>
      <da-svg src="/graphics/arrow.svg" class="go-modal__arrow first"/>
    </div>
    <h1><a href="https://go.daily.dev">go.daily.dev</a></h1>
    <p>You can enjoy Daily on your mobile device as well. Give it a try!</p>
  </da-modal>
</template>

<script>
import DaModal from '@daily/components/src/components/DaModal.vue';
import DaSvg from './DaSvg.vue';

export default {
  name: 'DaGo',
  components: {
    DaModal,
    DaSvg,
  },
};
</script>

<style>
.go-modal.modal .modal__container {
  background: linear-gradient(134.72deg, var(--color-cabbage-70) 0%, var(--color-onion-70) 100%);

  & .go-modal__graphics {
    position: relative;
    display: flex;
    flex-direction: row;
    align-items: center;
    padding: 0 22px;
    align-self: stretch;

    &:before {
      content: '';
      position: absolute;
      left: 0;
      right: 0;
      top: 0;
      bottom: 0;
      width: 100%;
      height: 110px;
      margin: auto 0;
      background: linear-gradient(270deg,
      rgba(169, 171, 179, 0) 0%, var(--color-salt-10) 50%, rgba(169, 171, 179, 0) 100%);
      opacity: 0.64;
      mix-blend-mode: overlay;
    }
  }

  & .go-modal__arrow {
    width: 38px;

    &.left {
      transform: rotate(180deg);
    }

    &.first {
      opacity: 0.16;
    }

    &.second {
      opacity: 0.24;
    }

    &.third {
      opacity: 0.32;
    }
  }

  & .go-modal__barcode {
    width: 123px;
    margin: 0 16px;
  }

  & h1 {
    text-transform: none;
  }
}
</style>
