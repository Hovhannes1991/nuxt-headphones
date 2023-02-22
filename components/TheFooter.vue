<template>
  <footer class="footer">
    <div class="logo cursor-pointer">
      <img src="icons/logo.svg" alt="logo" />
    </div>

    <nav>
      <li>Home</li>
      <li>About</li>
      <li>Product</li>
    </nav>

    <div class="social">
      <div class="img_wrapper flex-center cursor-pointer">
        <img src="icons/instagram.svg" alt="instagram" />
      </div>
      <div class="img_wrapper flex-center cursor-pointer">
        <img src="icons/twitter.svg" alt="twitter" />
      </div>
      <div class="img_wrapper flex-center cursor-pointer">
        <img src="icons/facebook.svg" alt="facebook" />
      </div>
    </div>
  </footer>
</template>

<style lang="scss" scoped>
footer {
  width: 100%;
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 62px 15%;
  background: var(--main-gradient);

  .logo {
    img {
      width: 70px;
    }
  }

  nav {
    display: flex;
    gap: 10px;

    li {
      color: #fff;
      list-style: none;
      cursor: pointer;
    }
  }

  .social {
    display: flex;
    gap: 15px;

    .img_wrapper {
      width: 50px;
      height: 50px;
      background-color: #fff;
      border-radius: 100%;
    }
  }

  @media only screen and (max-width: 1250px) {
    padding: 25px 45px;
    .logo {
      img {
        width: 50px;
      }
    }

    .social {
      gap: 12px;

      .img_wrapper {
        width: 40px;
        height: 40px;
        img {
          width: 18px;
          height: 18px;
        }
      }
    }
  }
}
</style>
