<template lang="pug">
  section.section-gravity-hub
    div.container-content
      div.block-gravity-hub
        h2.text.text-title Join the Gravity network!
        p.text Gravity is an open-source technology with transparent mechanisms for introducing changes and improvements. Join the community of open-source developers and service providers to contribute to the success of web3.0!
        span.button.button-orange(v-on:click="openModal()") Join us
</template>

<script>
export default {
  // mounted() {
  //   this.$root.$on("modalOpen", function(state) {
  //     console.log("open m", state);
  //     this.modalOpen = true;
  //   });
  // },
  methods: {
    openModal: function(state) {
      this.$root.$emit("modalLogin", true);
    }
  }
};
</script>

<style lang="scss" scoped>
@import "../../assets/scss/mixins/media.scss";

section.section-gravity-hub {
  display: flex;
  justify-content: center;
  margin-top: -150px;
  z-index: 1;

  @include b(tablet) {
    background: none;
    margin-top: -80px;
  }

  @include b(mobile) {
    margin-top: 0;
  }

  .container-content {
    max-width: 1000px;
    width: 100%;
    height: 1200px;
    justify-content: center;
    align-items: center;
    display: flex;
    z-index: 1;
    background: url("~static/img/space.svg") no-repeat center / 100%;

    @include bb(tablet, 0) {
      height: 650px;
    }

    @include b(tablet) {
      max-width: 650px;
    }

    @include b(mobile) {
      padding: 20px;
      height: auto;
      background: none;
    }

    @include b(mobile) {
      margin-bottom: 15px;
      font-size: 14px;
      line-height: 20px;
    }

    .block-gravity-hub {
      width: 100%;
      max-width: 555px;
      z-index: 1;

      @include bb(tablet, 0) {
        max-width: 325px;
      }

      @include b(mobile) {
        max-width: 100%;
      }

      .text {
        margin-bottom: 20px;
        font-size: 17px;
        line-height: 28px;
        opacity: 0.74;
        padding: 0 35px;
        text-align: center;

        @include b(tablet) {
          margin-bottom: 15px;
          font-size: 14px;
          line-height: 20px;
          padding: 0;
        }

        &-title {
          text-align: center;
          width: 100%;
          font-size: 48px;
          line-height: 50px;
          margin-bottom: 40px;
          opacity: 0.8;

          @include bb(tablet, 0) {
            font-size: 30px;
            line-height: 20px;
            margin-bottom: 30px;
          }

          @include b(mobile) {
            font-size: 25px;
            line-height: 20px;
            margin-bottom: 30px;
          }

          @include b(tablet) {
            opacity: 1;
          }
        }
      }

      .button {
        text-align: center;
        width: 100%;
        max-width: 270px;
        height: 50px;
        margin: 0 auto;
        color: white;
        margin-top: 30px;
        z-index: 1;
        position: absolute;
        left: 0;
        right: 0;

        @include b(tablet) {
          max-width: 160px;
          margin-top: 10px;
          font-size: 14px;
        }

        @include b(mobile) {
          max-width: 320px;
          margin-top: 10px;
          width: calc(100vw - 40px);
        }
      }

      .img-block {
        width: 100%;
        z-index: 0;
        display: block;
        margin-top: 50px;
        text-align: center;

        @include b(500) {
          text-align: center;
          display: flex;
          justify-content: center;
          align-items: center;
          margin-top: 20px;
        }

        img {
          &:nth-child(1) {
            @include b(500) {
              display: none;
              max-width: 450px;
            }
          }

          &:nth-child(2) {
            display: none;

            @include b(500) {
              display: block;
              max-width: 320px;
              margin-top: 60px;
            }
          }
        }
      }
    }
  }
}
</style>
