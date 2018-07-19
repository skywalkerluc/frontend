<template>
  <div class="content">
    <section class="login">
      <div class="login-form">
        <form>
          <div class="input-field">
            <input
              id="first_name"
              type="text">
            <label for="first_name">Email</label>
          </div>
          <div class="input-field">
            <input
              id="first_name"
              type="password">
            <label for="first_name">Senha</label>
          </div>

          <section class="recover-password">
            <a href="#">Esqueci minha senha</a>
          </section>

          <section class="actions">
            <button class="btn waves-effect waves-light">
              Entrar
            </button>
          </section>
        </form>

        <div class="or">Ou</div>

        <section class="social-buttons">
          <button class="btn waves-effect waves-light facebook">
            Logar com facebook
          </button>
        </section>
      </div>
    </section>
    <section class="splash" />
  </div>
</template>

<script>
export default {
}
</script>

<style lang="scss">
html, body, #__nuxt, #__layout {
  height: 100%;
}

.content {
  display: flex;
  height: 100%;

  .splash {
    background-color: #0077c2;
    width: 50%;
  }

  .login {
    width: 50%;
    display: flex;
    justify-content: center;
    align-items: center;
    flex-wrap: wrap;

    .login-form {
      padding: 15px;
      background: #FFF;
      width: 70%;

      .recover-password {
        text-align: right;
      }

      .actions {
        margin-top: 20px;

        button {
          width: 100%;
        }
      }
    }

    .or {
      text-align: center;
      color: #b0bec5;
      font-weight: bold;
    }

    .or, .social-buttons {
      margin-top: 25px;
    }

    .social-buttons {
      button {
        width: 100%;
      }

      .facebook {
        background: #32508E;
      }
    }
  }
}
</style>
