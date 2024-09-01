<template>
  <div class="facebook-login">
    <div class="content-wrapper">
      <div class="logo-container">
        <img src="../../assets/facebook.svg" alt="Facebook" class="logo" />
        <p class="slogan">O Facebook ajuda você a se conectar e compartilhar com as pessoas que fazem parte da sua vida.</p>
      </div>
      <div class="login-container">
        <form @submit.prevent="handleSubmit" class="form-login">
          <input v-model="email" type="text" placeholder="Email ou telefone" />
          <input v-model="password" type="password" placeholder="Senha" />
          <button type="submit" class="btn-login">Entrar</button>
          <a href="#" class="forgot-password">Esqueceu a senha?</a>
          <hr />
          <button type="button" class="btn-create-account">Criar nova conta</button>
        </form>
        <p class="create-page">
          <a href="#" class="link-create">Crie uma Página</a> para uma celebridade, uma marca ou uma empresa.
        </p>
      </div>
    </div>
  </div>
</template>

<script lang="ts">
import { defineComponent, ref } from 'vue';

export default defineComponent({
    name: 'FacebookLogin',
    setup(){
        const email = ref('')
        const password = ref('')

        const handleSubmit = () => {
          console.log('Login submitted:', { email: email.value, password: password.value })
        }
        return {
            email,
            password,
            handleSubmit
        }
    }
})

</script>

<style>
.facebook-login {
  display: flex;
  justify-content: center;
  align-items: center;
  height: 100vh;
}

.content-wrapper {
  display: flex;
  justify-content: space-between;
  align-items: center;
  width: 980px;
}

.logo {
  height: 106px;
  margin: -28px;
}

.slogan {
  font-size: 28px;
  line-height: 32px;
  width: 500px;
}

.login-container {
  width: 396px;
  
}

.form-login {
  display: flex;
  flex-direction: column;
  background-color: #fff;
  border-radius: 8px;
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1), 0 8px 16px rgba(0, 0, 0, 0.1);
  padding: 20px;
  text-align: center;
}

input {
  height: 50px;
  padding: 14px 16px;
  font-size: 17px;
  border-radius: 6px;
  border: 1px solid #dddfe2;
  margin-bottom: 12px;
  width: 100%;
  box-sizing: border-box;
}

.btn-login {
  background-color: #0866ff;
  cursor: pointer;
  border: none;
  border-radius: 6px;
  color: #fff;
  font-size: 20px;
  font-weight: bold;
  padding: 0 16px;
  height: 48px;
  margin-top: 6px;
  transition: 0.5s
}

.btn-login:hover {
  background-color: #1877f2;
  transition: 0.5s
}

.forgot-password {
  color: #1877f2;
  font-size: 14px;
  margin: 16px 0;
  text-decoration: none;
  display: inline-block;
}

.forgot-password:hover {
  text-decoration: underline
}

hr {
  border: none;
  border-top: 1px solid #dadde1;
  margin: 20px 0;
}

.btn-create-account {
  background-color: rgb(66, 183, 42);
  border: none;
  border-radius: 6px;
  color: #fff;
  font-size: 17px;
  font-weight: bold;
  padding: 0 16px;
  height: 48px;
  margin: 6px auto;
  cursor: pointer;
  transition: 0.5s
}

.btn-create-account:hover {
  background-color: rgb(48, 168, 24);
  transition: 0.5s
}

.create-page {
  color: #1c1e21;
  font-size: 14px;
  margin-top: 28px;
  text-align: center
}

.link-create {
  color: #1c1e21;
  text-decoration: none;
  font-weight: 600
}

.link-create:hover {
  text-decoration: underline
}

@media screen and (max-width: 900px){
  .content-wrapper {
    display: flex;
    justify-content: center;
    align-items: center;
    text-align: center;
    flex-direction: column
  }
  .slogan {
    display: flex;
    flex-wrap: wrap;
  }
}
</style>