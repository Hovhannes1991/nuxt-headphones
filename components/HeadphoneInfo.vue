<template>
  <div class="headphone_info">
    <div class="left_section">
      <h2 class="subtitle">
        Good headphones<br />
        and loud music<br />
        is all you need
      </h2>

      <div class="info">
        <div class="info_item">
          <div class="icon">
            <img src="icons/battery.svg" alt="battery" />
          </div>
          <div class="info_data_wrapper">
            <div class="name">Battery</div>
            <div class="info_text">Battery 6.2V-AAC Codec</div>
            <div class="learn_more">Learn more</div>
          </div>
        </div>
        <div class="info_item">
          <div class="icon">
            <img src="icons/bluetooth.svg" alt="bluetooth" />
          </div>
          <div class="info_data_wrapper">
            <div class="name">Bluetooth</div>
            <div class="info_text">Bluetooth-3 Super</div>
            <div class="learn_more">Learn more</div>
          </div>
        </div>
        <div class="info_item">
          <div class="icon">
            <img src="icons/microphone.svg" alt="microphone" />
          </div>
          <div class="info_data_wrapper">
            <div class="name">Microphone</div>
            <div class="info_text">Default Microphone</div>
            <div class="learn_more">Learn more</div>
          </div>
        </div>
      </div>
    </div>

    <div class="image_container">
      <img
        class="sound_icon_left"
        :src="'icons/sound-wave-left.png'"
        alt="icon"
      />
      <img
        class="headphone_image"
        :src="'images/headphone-yellow.svg'"
        alt="headphone"
      />
      <img
        class="sound_icon_right"
        :src="'icons/sound-wave-right.png'"
        alt="icon"
      />
    </div>
  </div>
</template>

<style lang="scss" scoped>
.headphone_info {
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  margin: 0 auto;
  background-color: #fff;

  .left_section {
    .subtitle {
      color: #180202;
      font-weight: 700;
      font-size: 2.5rem;
      margin-bottom: 50px;
    }

    .info {
      display: flex;
      flex-direction: column;
      gap: 20px;

      .info_item {
        display: flex;
        align-items: flex-start;
        gap: 20px;

        .name {
          color: #180202;
          font-size: 31px;
          font-weight: 500;
          line-height: 43px;
        }

        .info_text {
          color: #180202;
          font-size: 16px;
          font-weight: 400;
          line-height: 24px;
        }

        .learn_more {
          color: #ff4948;
          font-size: 16px;
          font-weight: 500;
          line-height: 24px;
        }
      }
    }
  }

  .image_container {
    // width: 500px;
    display: flex;
    align-items: flex-end;

    .sound_icon_left {
      transform: translate(58px, 58px);
    }

    .sound_icon_right {
      transform: translate(-44px, 58px);
    }

    @media only screen and (max-width: 1400px) {
      .headphone_image {
        width: 250px;
      }
      .sound_icon_left {
        width: 100px;
        transform: translate(44px, 58px);
      }
      .sound_icon_right {
        width: 100px;
        transform: translate(-34px, 58px);
      }
    }
  }
}
</style>
