# wdev-site
  # api no repo
    https://github.com/william-costa/wdev-mock-site-resources

# para criar o projeto
    - vue ui
      - criar
      - criar novo projeto
      - npm or yarn
      - (proximo) definicao padrao
      - criar projeto

    - ou
      - vue create wdev-site`

## Project setup
```
npm install
```

### Compiles and hot-reloads for development
```
npm run serve
```

### Compiles and minifies for production
```
npm run build
```

### Lints and fixes files
```
npm run lint
```

### Sobre o desenvolvimento
  - temos que criar primeiro a tela para mobile

  - map:
  - src
    - components:
      -> Header
      -> Home
      -> Footer
      ..
    - services
    - routes
      -- api (o axios vai esta aqui, pegando nossa api)
      ..
      -> Videos
      -> Sobre

  - coponente principal:
    - App.vue
      - vamos pegar todos os nosso components e importar dentro

  - header
    - bem interessante, mexemos com func, if,
    fizemos a rega do menu

  - home 
    - muito simples, houve apenas html e css

  - footer
    - estilo simples e direto
    - vms fazer nosso primeira consulta com axios, isntalar
      - npm i axios
    - caminho = @ fica na pasta: src
    - veja como foi feito a chamada na api e como foi simples 
    pegar os dados, muito interessante

  - Vue router (routes)
    - npm i vue-router
    - as configuracoes do `router`é bem interessante
    - depois de todo configurado vamos passar para o `main.js`
    - em seguida vms para de `App.vue` o component `Home`e add `router-view`como mostra no proprio component

  - Videos
    - nao teve muito segredo ou algo de diferente, apenas css
    e chamada na api da msm forma do `Footer`, de boa

  - Sobre
    - n teve muita coisa de diferente
    - apenas a chamada na api pegando textos em json com html dentro
    - vimos como podemos processar o html junto ao texto. v-html=" "

  OBS:
    - o Vue pode atualizar apenas aonde foi alterado, isso é bom
    - trocar `a`por `router-link to=" "` do `Header`
