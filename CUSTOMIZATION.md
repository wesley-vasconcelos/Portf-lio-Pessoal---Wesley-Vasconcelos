# Guia de Personalização do Portfólio

Este documento contém instruções para personalizar e expandir o portfólio de Wesley Vasconcelos.

## 🎨 Personalizando Cores e Temas

### Variáveis CSS
As cores principais estão definidas em `src/App.vue` nas variáveis CSS:

```css
:root {
  --primary-color: #3b82f6;      /* Azul principal */
  --secondary-color: #1e40af;    /* Azul escuro */
  --accent-color: #06b6d4;       /* Ciano */
  --text-primary: #1f2937;       /* Texto principal */
  --text-secondary: #6b7280;     /* Texto secundário */
  /* ... outras variáveis */
}
```

### Gradientes
Os gradientes são usados extensivamente. Para alterar:
- Hero sections: `linear-gradient(135deg, #667eea 0%, #764ba2 100%)`
- Botões: `linear-gradient(135deg, var(--primary-color), var(--accent-color))`
- Ícones: Cada tecnologia tem seu gradiente específico

## 📝 Atualizando Conteúdo

### Informações Pessoais
Edite os seguintes arquivos para atualizar informações:

1. **src/views/HomeView.vue** - Página inicial
2. **src/views/AboutView.vue** - Sobre mim
3. **src/views/ExperienceView.vue** - Experiência profissional
4. **src/views/ContactView.vue** - Informações de contato

### Adicionando Nova Experiência
No arquivo `src/views/ExperienceView.vue`, adicione um novo item na timeline:

```vue
<div class="timeline-item">
  <div class="timeline-marker current"></div> <!-- Remove 'current' se não for o atual -->
  <div class="timeline-content">
    <div class="job-header">
      <h3>Título do Cargo</h3>
      <span class="company">Nome da Empresa</span>
      <span class="period">Período</span>
      <span class="location">Localização</span>
    </div>
    <!-- ... resto do conteúdo -->
  </div>
</div>
```

### Adicionando Novas Habilidades
No arquivo `src/views/SkillsView.vue`, adicione um novo card:

```vue
<div class="skill-card">
  <div class="skill-icon nova-tech">TECH</div>
  <h3>Nova Tecnologia</h3>
  <div class="skill-level">
    <div class="level-bar">
      <div class="level-fill" style="width: 80%"></div>
    </div>
    <span class="level-text">Avançado</span>
  </div>
  <p>Descrição da tecnologia</p>
  <div class="experience-years">X+ anos</div>
</div>
```

E adicione o CSS correspondente:
```css
.skill-icon.nova-tech {
  background: linear-gradient(135deg, #cor1, #cor2);
}
```

## 🖼️ Adicionando Imagens

### Avatar/Foto de Perfil
Para adicionar uma foto real:

1. Coloque a imagem em `public/images/`
2. Substitua o avatar em `src/views/HomeView.vue`:

```vue
<!-- Substitua -->
<div class="profile-avatar">
  <span class="avatar-text">WV</span>
</div>

<!-- Por -->
<div class="profile-avatar">
  <img src="/images/wesley-avatar.jpg" alt="Wesley Vasconcelos" />
</div>
```

3. Adicione o CSS:
```css
.profile-avatar img {
  width: 100%;
  height: 100%;
  object-fit: cover;
  border-radius: 50%;
}
```

### Logos de Empresas
Adicione logos reais das empresas em `public/images/companies/` e atualize os componentes.

## 🔗 Configurando Links Reais

### Links de Contato
Atualize os links em `src/views/ContactView.vue`:

```vue
<!-- Email -->
<a href="mailto:seu.email@real.com" class="contact-link">
  Enviar Email
</a>

<!-- LinkedIn -->
<a href="https://linkedin.com/in/seu-perfil-real" target="_blank" class="contact-link">
  Ver Perfil
</a>

<!-- GitHub -->
<a href="https://github.com/seu-usuario-real" target="_blank" class="contact-link">
  Ver Repositórios
</a>
```

## 📱 Adicionando Novas Seções

### Seção de Projetos
1. Crie `src/views/ProjectsView.vue`
2. Adicione a rota em `src/router/index.ts`
3. Adicione o link no `src/components/NavBar.vue`

### Seção de Blog
1. Crie `src/views/BlogView.vue`
2. Configure roteamento dinâmico para posts individuais
3. Integre com um CMS headless (Strapi, Contentful, etc.)

## 🚀 Funcionalidades Avançadas

### Formulário de Contato Funcional
Para tornar o formulário funcional, integre com:

1. **EmailJS** - Envio direto do frontend
2. **Netlify Forms** - Se hospedado no Netlify
3. **API própria** - Backend personalizado

Exemplo com EmailJS:
```javascript
import emailjs from '@emailjs/browser'

const submitForm = async () => {
  try {
    await emailjs.send(
      'service_id',
      'template_id',
      form,
      'public_key'
    )
    // Sucesso
  } catch (error) {
    // Erro
  }
}
```

### Animações
Adicione animações com:
- **Framer Motion** para Vue
- **GSAP**
- **Lottie** para animações complexas

### Internacionalização
Para suporte a múltiplos idiomas:
1. Instale `vue-i18n`
2. Configure arquivos de tradução
3. Adicione seletor de idioma

## 🔧 Otimizações

### Performance
- Lazy loading de imagens
- Code splitting por rotas
- Compressão de assets
- Service Workers para cache

### SEO
- Meta tags dinâmicas
- Sitemap.xml
- Schema.org markup
- Open Graph tags

### Analytics
Adicione Google Analytics ou similar:
```javascript
// main.ts
import { gtag } from 'vue-gtag'

app.use(gtag, {
  config: {
    id: 'GA_MEASUREMENT_ID'
  }
})
```

## 📦 Deploy

### Netlify
1. Build: `npm run build`
2. Publish directory: `dist`
3. Configure redirects para SPA

### Vercel
1. Conecte o repositório
2. Configure build command: `npm run build`
3. Output directory: `dist`

### GitHub Pages
1. Configure GitHub Actions
2. Build e deploy automático
3. Configure domínio customizado

## 🛠️ Manutenção

### Atualizações Regulares
- Dependências: `npm update`
- Informações de experiência
- Novas habilidades
- Projetos recentes

### Backup
- Mantenha o código no Git
- Backup das imagens
- Documentação atualizada

---

Para dúvidas ou sugestões, consulte a documentação oficial do Vue.js e das tecnologias utilizadas.
