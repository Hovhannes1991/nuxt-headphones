<template>
  <div class="subscribe_section">
    <h2 class="section_title">Subscribe</h2>
    <p>Lorem ipsum dolor sit amet consectetur adipisicing elit.</p>

    <div class="submit_section">
      <input type="text" placeholder="Enter Your email address" />
      <button>Subscribe</button>
    </div>
  </div>
</template>

<style lang="scss" scoped>
.subscribe_section {
  min-width: 400px;
  width: 100%;
  max-width: 712px;
  margin: 0 auto;
  background-color: #fff4f4;
  border-radius: 20px;
  padding: 5% 7%;
  text-align: center;

  .submit_section {
    margin: 55px auto 0 auto;
    height: 55px;
    max-width: 500px;
    background-color: #fff;
    border-radius: 44px;
    display: flex;
    justify-content: space-between;
    padding: 0 0 0 30px;

    input {
      font-size: 18px;
      border: none;
      outline: none;
      width: 100%;
      padding-right: 10px;
    }

    button {
      font-size: 22px;
      font-weight: 500;
      background: #ff4948;
      color: #fff;
      border-radius: 50px;
      border: none;
      outline: none;
      padding: 15px 30px;
      cursor: pointer;
      transition: background-color 0.3s linear;

      &:hover {
        background-color: #f90e0e;
      }
    }
  }
}
</style>
