<template>
  <div class="login">
    <div class="login__background"></div>
    <div class="login__form">
      <h3 class="login__form_title">
        Sign in
      </h3>
      <span class="login__form_description">
        Sign in to your account using email and password provided during registration.
      </span>
      <label class="login__form_label" for="email">Email</label>
      <input class="login__form_input" name="email" type="email" placeholder="Your working email">
      <label class="login__form_label" for="password">Password</label>
      <input class="login__form_input" name="password" type="password" placeholder="Your password">
      <button class="login__form_button">Sign in</button>
      <div class="login__form_not-account">
        <span class="login__form_not-account_question">
          Don't have an account?
        </span>
        <a class="login__form_not-account_link" href="#">
          Sign up
        </a>
      </div>
    </div>
  </div>  
</template>

<script>
  export default {
    
  }
  
</script>

<style lang="scss">
  .login {
    &__background {
      position: absolute;
      width: 100%;
      height: 100%;
      top: 0;
      bottom: 0;
      right: 0;
      left: 0;
      background-color: #1E212C;
      opacity: 0.75;
    }
    &__form {
      position: absolute;
      display: flex;
      flex-direction: column;
      max-width: 490px;
      width: 100%;
      margin: auto 0;
      left: 50%;
      margin-left: -245px;
      padding: 50px;
      border-radius: 4px;
      border: 1px solid #E5E8ED;
      background: #FFF;
      box-shadow: 0px 4px 4px -4px rgba(30, 33, 44, 0.05), 0px 12px 10px -6px rgba(30, 33, 44, 0.08), 0px 26px 24px -10px rgba(30, 33, 44, 0.10), 0px 60px 80px -20px rgba(30, 33, 44, 0.16);
      &_title {
        margin-bottom: 24px;
        text-align: center;
        font-size: 28px;
        font-weight: 700;
        line-height: 150%;
        color: #1E212C;
      }
      &_description {
        display: flex;
        width: 100%;
        text-align: center;
        font-size: 14px;
        font-weight: 400;
        line-height: 150%;
        color: #787A80;
      }
      &_label {
        margin-top: 20px;
        font-size: 14px;
        font-weight: 400;
        line-height: 150%;
        color: #424551;
      }
      &_input {
        margin-top: 8px;
        width: 100%;
        height: 44px;
        padding: 0px 16px;
        font-size: 14px;
        font-weight: 400;
        line-height: 150%;
        border-radius: 4px;
        border: 1px solid #D7DADD;
        color: #9A9CA5;
        background: #FFF;
      }
      &_button {
        margin: 24px 0px;
        width: 100%;
        height: 44px;
        padding: 0px 32px;
        font-size: 14px;
        font-weight: 700;
        line-height: 44px;
        letter-spacing: 0.5px;
        border-radius: 4px;
        color: #FFF;
        background-color: #17696A;
      }
      &_button:hover {
        transition: all ease-in-out 0.3s;
        background-color: #0f4647;
      }
      &_not-account {
        display: flex;
        &_question {
          font-size: 14px;
          font-weight: 400;
          line-height: 150%;
          color: #424551;
        }
        &_link {
          margin-left: 5px;
          font-size: 14px;
          font-weight: 400;
          line-height: 150%;
          color: #17696A;
        }
        &_link:hover {
          border-bottom: 1px solid #17696A;
        }
      }
    }
  }
</style>