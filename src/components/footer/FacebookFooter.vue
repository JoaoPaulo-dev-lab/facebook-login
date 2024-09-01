<template>
    <footer class="footer">
      <div class="footer-languages">
        <a v-for="link in languageLinks" :key="link.text" :href="link.url">{{ link.text }}</a>
      </div>
      <hr>
      <div class="footer-sections">
        <div class="footer-section" v-for="section in footerSections" :key="section.title">
          <a v-for="link in section.links" :key="link.text" :href="link.url">{{ link.text }}</a>
        </div>
      </div>
      <div class="footer-copyright">
        Meta © 2024
      </div>
    </footer>
  </template>
  
  <script lang="ts">
  import { defineComponent } from 'vue';
  
  export default defineComponent({
    name: 'FacebookFooter',
    data() {
      return {
        languageLinks: [
          { text: 'Português (Brasil)', url: '#' },
          { text: 'English (US)', url: '#' },
          { text: 'Español', url: '#' },
          { text: 'Français (France)', url: '#' },
          { text: 'Italiano', url: '#' },
          { text: 'Deutsch', url: '#' },
          { text: 'العربية', url: '#' },
          { text: 'हिन्दी', url: '#' },
          { text: '中文(简体)', url: '#' },
          { text: '日本語', url: '#' },
        ],
        footerSections: [
          {
            title: 'Main',
            links: [
              { text: 'Cadastre-se', url: '#' },
              { text: 'Entrar', url: '#' },
              { text: 'Messenger', url: '#' },
              { text: 'Facebook Lite', url: '#' },
              { text: 'Video', url: '#' },
              { text: 'Locais', url: '#' },
              { text: 'Jogos', url: '#' },
              { text: 'Marketplace', url: '#' },
              { text: 'Meta Pay', url: '#' },
              { text: 'Meta Store', url: '#' },
            ]
          },
          {
            title: 'Meta',
            links: [
              { text: 'Meta Quest', url: '#' },
              { text: 'Meta Ray-Ban', url: '#' },
              { text: 'Meta AI', url: '#' },
              { text: 'Sobre', url: '#' },
              { text: 'Criar anúncio', url: '#' },
              { text: 'Criar Página', url: '#' },
              { text: 'Desenvolvedores', url: '#' },
              { text: 'Carreiras', url: '#' },
              { text: 'Cookies', url: '#' },
              { text: 'Escolhas para anúncios', url: '#' },
            ]
          },
          {
            title: 'Legal',
            links: [
              { text: 'Termos', url: '#' },
              { text: 'Ajuda', url: '#' },
              { text: 'Política de Privacidade', url: '#' },
              { text: 'Central de Privacidade', url: '#' },
              { text: 'Grupos', url: '#' },
              { text: 'Carregamento de contatos e não usuários', url: '#' },
            ]
          }
        ]
      };
    },
  });
  </script>
  
  <style scoped>
  .footer {
  background-color: #f9f9f9;
  padding: 20px 0;
  font-size: 12px;
  color: #666;
  text-align: center;
  display: inline-block
}

.footer-languages a {
  padding-left: 20px;
  color: #666;
  text-decoration: none;
  display: inline-block;
}

.footer-languages a:hover {
  text-decoration: underline;
}


.footer-sections a {
  padding-left: 20px;
  color: #666;
  text-decoration: none;
  display: inline-block
}

.footer-sections a:hover {
  text-decoration: underline;
}

.footer-copyright {
  margin-top: 10px;
  color: #999;
}
  </style>