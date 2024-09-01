<template>
    <footer class="facebook-footer">
        <div class="container">
            <div class="language-list">
                <a v-for="language in languages" :key="language" href="#">{{ language }}</a>
                <button class="add-language">+</button>
            </div>
            <hr>
            <div class="links-list">
                <a v-for="link in links" :key="link" href="#">{{ link }}</a>
            </div>
            <span class="copyright">Meta © {{ currentYear }}</span>
        </div>
    </footer>
</template>

<script lang="ts">
import { defineComponent, ref } from 'vue';

export default defineComponent({
  name: 'FacebookFooter',
  setup() {
    const languages = [
      'Português (Brasil)', 
      'English (US)', 'Español', 
      'Français (France)', 
      'Italiano', 
      'Deutsch', 
      'العربية', 
      'हिन्दी', 
      '中文(简体)', 
      '日本語'
    ];

    const links = [
      'Cadastre-se', 
      'Entrar', 
      'Messenger', 
      'Facebook Lite', 
      'Vídeo', 
      'Locais', 
      'Jogos', 
      'Marketplace', 
      'Meta Pay', 
      'Meta Store', 
      'Meta Quest', 
      'Meta Ray-Ban', 
      'Meta AI', 
      'Instagram', 
      'Threads', 
      'Campanhas de arrecadação de fundos', 
      'Serviços', 
      'Central de Informações de Votação', 
      'Política de Privacidade', 
      'Central de Privacidade', 
      'Grupos', 
      'Sobre', 
      'Criar anúncio', 
      'Criar Página', 
      'Desenvolvedores', 
      'Carreiras', 
      'Cookies', 
      'Escolhas para anúncios', 
      'Termos', 
      'Ajuda', 
      'Carregamento de contatos e não usuários'
    ];

    const currentYear = ref(new Date().getFullYear())

    return { 
        languages, 
        links,
        currentYear
    };
  },
});
</script>

<style scoped>
.facebook-footer {
  background-color: white;
  color: #8a8d91;;
  font-size: 12px;
  padding: 20px 0;
  display: flex;
  flex-wrap: wrap;
}

.container {
  max-width: 980px;
  margin: 0 auto;
  padding: 0 16px;
}

.language-list {
  margin-bottom: 8px;
}

.language-list a, .links-list a {
  color: #8a8d91;;
  text-decoration: none;
  margin-right: 10px;
}

.language-list a:hover, .links-list a:hover {
  text-decoration: underline;
}

.add-language {
  background: none;
  border: 1px solid;
  border-radius: 2px;
  padding: 0 8px;
  color: #8a8d91;;
  cursor: pointer;
  font-size: 12px;
}

.links-list {
  line-height: 1.6;
}

.copyright {
  display: flex;
  margin-top: 20px;
}
</style>