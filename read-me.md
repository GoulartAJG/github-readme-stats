<p align="center">Gostou do projeto? Por favor, considere <a href="https://www.paypal.me/GoulartAJG">doar</a> para ajudar a melhorar!

# Recursos

- [Cartão de estatísticas do GitHub](#github-stats-card)
- [GitHub Extra Pins](#github-extra-pins)
- [Top Languages ​​Card](#top-languages-card)
- [Estatísticas da Semana Wakatime](#wakatime-week-stats)
- [Temas](#temas)
- [Personalização](#customização)
  - [Opções comuns](#common-options)
  - [Opções exclusivas do cartão de estatísticas](#stats-card-exclusive-options)
  - [Opções exclusivas do cartão Repo](#repo-card-exclusive-options)
  - [Opções exclusivas do cartão de idioma](#language-card-exclusive-options)
  - [Opção exclusiva do cartão Wakatime](#wakatime-card-exclusive-options)
- [Implantar você mesmo](#implantar-em-sua-própria-instância-vercel)

# Cartão de estatísticas do GitHub

Copie e cole isso em seu conteúdo de markdown e pronto. Simples!

Altere o valor `?username=` para o nome de usuário do seu GitHub.

``` md
[![Estatísticas do GitHub do Alan](https://github-readme-stats.vercel.app/api?username=GoulartAJG)](https://github.com/GoulartAJG/github-readme-stats)
```

_Observação: as classificações disponíveis são S+ (1º superior), S (25º superior%), A++ (45º superior), A+ (60º superior) e B+ (todos).
Os valores são calculados usando a [função de distribuição cumulativa](https://en.wikipedia.org/wiki/Cumulative_distribution_function) usando confirmações, contribuições, problemas, estrelas, solicitações pull, seguidores e repositórios próprios.
A implementação pode ser investigada em [src/calculateRank.js](./src/calculateRank.js)._

### Escondendo estatísticas individuais

Para ocultar quaisquer estatísticas específicas, você pode passar um parâmetro de consulta `?hide=` com valores separados por vírgula.

> Opções: `&hide=stars,commits,prs,issues,contribs`

``` md
![Estatísticas do GitHub Alan](https://github-readme-stats.vercel.app/api?username=GoulartAJG&hide=contribs,prs)
```

### Adicionando a contagem de contribuições privadas à contagem total de commits

Você pode adicionar a contagem de todas as suas contribuições privadas à contagem total de commits usando o parâmetro de consulta `?count_private=true`.

_Observação: Se você mesmo estiver implantando este projeto, as contribuições privadas serão contadas por padrão. Caso contrário, você precisa optar por compartilhar suas contagens de contribuições privadas._

> Opções: `&count_private=true`

``` md
![Estatísticas do GitHub Alan](https://github-readme-stats.vercel.app/api?username=GoulartAJG&count_private=true)
```

### Mostrando ícones

Para habilitar ícones, você pode passar `show_icons=true` no parâmetro de consulta, assim:

``` md
![Estatísticas do GitHub Alan](https://github-readme-stats.vercel.app/api?username=GoulartAJG&show_icons=true)
```

### Temas

Com temas embutidos, você pode personalizar a aparência do cartão sem fazer nenhuma [personalização manual](#customization).

Use o parâmetro `&theme=THEME_NAME` assim:-

``` md
![Estatísticas do GitHub Alan](https://github-readme-stats.vercel.app/api?username=GoulartAJG&show_icons=true&theme=radical)
```

#### Todos os temas embutidos: -

dark, radical, merko, gruvbox, tokyonight, onedark, cobalt, synthwave, highcontrast, dracula

<img src="https://res.cloudinary.com/GoulartAJG/image/upload/v1595174536/grs-themes_l4ynja.png" alt="GitHub Readme Stats Themes" width="600px"/>

Você pode ver uma prévia de [todos os temas disponíveis](./themes/README.md) ou verificar o [arquivo de configuração do tema](./themes/index.js) e **você também pode contribuir com novos temas** se você gostou

### Costumização

Você pode personalizar a aparência do seu `Stats Card` ou `Repo Card` como desejar com os parâmetros de URL.

#### Opções comuns:

- `title_color` - Cor do título do cartão _(cor hexadecimal)_
- `text_color` - Cor do texto do corpo _(cor hexadecimal)_
- `icon_color` - Cor dos ícones se disponível _(cor hexadecimal)_
- `border_color` - Cor da borda do cartão _(cor hexadecimal)_. (Não se aplica quando `hide_border` está habilitado)
- `bg_color` - A cor de fundo do cartão _(hex color)_ **ou** um gradiente na forma de _angle,start,end_
- `hide_border` - Esconde a borda do cartão _(boolean)_
- `theme` - nome do tema, escolha entre [todos os temas disponíveis](./themes/README.md)
- `cache_seconds` - define o cabeçalho do cache manualmente _(min: 1800, max: 86400)_
- `locale` - define o idioma no cartão _(por exemplo, cn, de, es, etc.)_
- `border_radius` - Arredondamento de cantos no cartão_

##### Gradiente em bg_color

Você pode fornecer vários valores separados por vírgula na opção bg_color para renderizar um gradiente, o formato do gradiente é: -

```
&bg_color=DEG,COLOR1,COLOR2,COLOR3...COLOR10
```

> Nota sobre o cache: os cartões Repo têm um cache padrão de 4 horas (14.400 segundos) se a contagem de garfos e estrelas for inferior a 1k, caso contrário, são 2 horas (7.200 segundos). Além disso, observe que o cache é limitado a um mínimo de 2 horas e um máximo de 24 horas.

#### Opções Exclusivas do Cartão de Estatísticas:

- `hide` - Oculta os itens especificados das estatísticas _(valores separados por vírgula)_
- `hide_title` - _(boolean)_
- `hide_rank` - _(boolean)_ oculta a classificação e redimensiona automaticamente a largura do cartão
- `show_icons` - _(boolean)_
- `include_all_commits` - Conta o total de commits em vez de apenas os commits do ano atual _(boolean)_
- `count_private` - Contar commits privados _(boolean)_
- `line_height` - Define a altura da linha entre o texto _(number)_
- `custom_title` - Define um título personalizado para o cartão
- `disable_animations` - Desativa todas as animações no cartão _(boolean)_

#### Opções Exclusivas do Cartão Repo:

- `show_owner` - Mostra o nome do proprietário do repositório _(boolean)_

#### Opções Exclusivas do Cartão de Idioma:

- `hide` - Oculta os idiomas especificados do cartão _(valores separados por vírgula)_
- `hide_title` - _(boolean)_
- `layout` - Alterna entre dois layouts disponíveis `default` e `compact`
- `card_width` - Defina a largura do cartão manualmente _(number)_
- `langs_count` - Mostrar mais idiomas no cartão, entre 1-10, o padrão é 5 _(número)_
- `exclude_repo` - Excluir repositórios especificados _(valores separados por vírgula)_
- `custom_title` - Define um título personalizado para o cartão

> :aviso: **Importante:**
> Os nomes dos idiomas devem ter escape uri, conforme especificado em [Percent Encoding](https://en.wikipedia.org/wiki/Percent-encoding)
> (ou seja: `c++` deve se tornar `c%2B%2B`, `jupyter notebook` deve se tornar `jupyter%20notebook`, etc.) Você pode usar
> [urlencoder.org](https://www.urlencoder.org/) para ajudá-lo a fazer isso automaticamente.

#### Opções Exclusivas do Cartão Wakatime:

- `hide` - Oculta os idiomas especificados do cartão _(valores separados por vírgula)_
- `hide_title` - _(boolean)_
- `line_height` - Define a altura da linha entre o texto _(number)_
- `hide_progress` - Oculta a barra de progresso e a porcentagem _(boolean)_
- `custom_title` - Define um título personalizado para o cartão
- `layout` - Alterna entre dois layouts disponíveis `default` e `compact`
- `langs_count` - Limite o número de idiomas no cartão, padrão para todos os idiomas relatados
- `api_domain` - Defina um domínio de API personalizado para o cartão, por exemplo, para usar serviços como [Hakatime](https://github.com/mujx/hakatime) ou [Wakapi](https://github.com/muety/ wakapi)
- `range` – Solicite um intervalo diferente do padrão do WakaTime, por exemplo, `last_7_days`. Consulte [documentos da API WakaTime](https://wakatime.com/developers#stats) para obter uma lista de opções disponíveis.

---

# Pins extras do GitHub

Os pinos extras do GitHub permitem que você fixe mais de 6 repositórios em seu perfil usando um perfil leia-me do GitHub.

Yay! Você não está mais limitado a 6 repositórios fixados.

### Uso

Copie e cole este código em seu readme e altere os links.

Endpoint: `api/pin?username=GoulartAJG&repo=github-readme-stats`

``` md
[![Cartão Leiame](https://github-readme-stats.vercel.app/api/pin/?username=GoulartAJG&repo=github-readme-stats)](https://github.com/GoulartAJG/github- readme-stats)
```

### Demonstração

[![Cartão Leiame](https://github-readme-stats.vercel.app/api/pin/?username=GoulartAJG&repo=github-readme-stats)](https://github.com/GoulartAJG/github- readme-stats)

Use a variável [show_owner](#customization) para incluir o nome de usuário do proprietário do repositório

[![Cartão Leiame](https://github-readme-stats.vercel.app/api/pin/?username=GoulartAJG&repo=github-readme-stats&show_owner=true)](https://github.com/GoulartAJG/ github-readme-stats)

# Cartão de principais idiomas

O cartão de idiomas principais mostra o idioma principal usado com mais frequência por um usuário do GitHub.

_NOTA: Top Languages ​​não indica meu nível de habilidade ou algo assim; é uma métrica do GitHub para determinar quais idiomas têm mais código no GitHub. É um novo recurso do github-readme-stats._

### Uso

Copie e cole este código em seu readme e altere os links.

Endpoint: `api/top-langs?username=GoulartAJG`

``` md
[![Top Langs](https://github-readme-stats.vercel.app/api/top-langs/?username=GoulartAJG)](https://github.com/GoulartAJG/github-readme-stats)
```

### Excluir repositórios individuais

Você pode usar o parâmetro `?exclude_repo=repo1,repo2` para excluir repositórios individuais.

``` md
[![Top Langs](https://github-readme-stats.vercel.app/api/top-langs/?username=GoulartAJG&exclude_repo=github-readme-stats,GoulartAJG.github.io)](https:// github.com/GoulartAJG/github-readme-stats)
```

### Ocultar idiomas individuais

Você pode usar o parâmetro `?hide=language1,language2` para ocultar idiomas individuais.

``` md
[![Top Langs](https://github-readme-stats.vercel.app/api/top-langs/?username=GoulartAJG&hide=javascript,html)](https://github.com/GoulartAJG/github- readme-stats)
```

### Mostrar mais idiomas

Você pode usar a opção `&langs_count=` para aumentar ou diminuir o número de idiomas mostrados no cartão. Os valores válidos são inteiros entre 1 e 10 (inclusive), e o padrão é 5.

``` md
[![Top Langs](https://github-readme-stats.vercel.app/api/top-langs/?username=GoulartAJG&langs_count=8)](https://github.com/GoulartAJG/github-readme- Estatísticas)
```

### Layout de cartão de idioma compacto

Você pode usar a opção `&layout=compact` para alterar o design do cartão.

``` md
[![Top Langs](https://github-readme-stats.vercel.app/api/top-langs/?username=GoulartAJG&layout=compact)](https://github.com/GoulartAJG/github-readme- Estatísticas)
```

### Demonstração

[![Top Langs](https://github-readme-stats.vercel.app/api/top-langs/?username=GoulartAJG)](https://github.com/GoulartAJG/github-readme-stats)

- Disposição compacta

[![Top Langs](https://github-readme-stats.vercel.app/api/top-langs/?username=GoulartAJG&layout=compact)](https://github.com/GoulartAJG/github-readme- Estatísticas)

# Estatísticas da Semana Wakatime

Altere o valor `?username=` para seu nome de usuário [Wakatime](https://wakatime.com).

``` md
[![estatísticas de wakatime de willianrod](https://github-readme-stats.vercel.app/api/wakatime?username=willianrod)](https://github.com/GoulartAJG/github-readme-stats)
```

### Demonstração

[![estatísticas de wakatime de willianrod](https://github-readme-stats.vercel.app/api/wakatime?username=willianrod)](https://github.com/GoulartAJG/github-readme-stats)

[![estatísticas de wakatime de willianrod](https://github-readme-stats.vercel.app/api/wakatime?username=willianrod&hide_progress=true)](https://github.com/GoulartAJG/github-readme-stats)

- Disposição compacta

[![estatísticas de wakatime de willianrod](https://github-readme-stats.vercel.app/api/wakatime?username=willianrod&layout=compact)](https://github.com/GoulartAJG/github-readme-stats)

---

### Todas as demonstrações

- Predefinição

![Estatísticas do GitHub Alan](https://github-readme-stats.vercel.app/api?username=GoulartAJG)

- Ocultar estatísticas específicas

![Estatísticas do GitHub Alan](https://github-readme-stats.vercel.app/api?username=GoulartAJG&hide=contribs,issues)

- Mostrando ícones

![Estatísticas do GitHub Alan](https://github-readme-stats.vercel.app/api?username=GoulartAJG&hide=issues&show_icons=true)

- Personalizar a cor da borda

![Estatísticas do GitHub Alan](https://github-readme-stats.vercel.app/api?username=GoulartAJG&border_color=2e4058)

- Incluir todos os commits

![Estatísticas do GitHub Alan](https://github-readme-stats.vercel.app/api?username=GoulartAJG&include_all_commits=true)

- Temas

Escolha um dos [temas padrão](#themes)

![Estatísticas do GitHub Alan](https://github-readme-stats.vercel.app/api?username=GoulartAJG&show_icons=true&theme=radical)

- Gradiente

![Estatísticas do GitHub Alan](https://github-readme-stats.vercel.app/api?username=GoulartAJG&bg_color=30,e96443,904e95&title_color=fff&text_color=fff)

- Personalização do cartão de estatísticas

![Estatísticas do GitHub Alan](https://github-readme-stats.vercel.app/api/?username=GoulartAJG&show_icons=true&title_color=fff&icon_color=79ff97&text_color=9f9f9f&bg_color=151515)

- Configurando a localidade do cartão

![Estatísticas do GitHub Alan](https://github-readme-stats.vercel.app/api/?username=GoulartAJG&locale=es)

- Personalizando o cartão de recompra

![Cartão personalizado](https://github-readme-stats.vercel.app/api/pin?username=GoulartAJG&repo=github-readme-stats&title_color=fff&icon_color=f9f9f9&text_color=9f9f9f&bg_color=151515)

- Principais idiomas

[![Top Langs](https://github-readme-stats.vercel.app/api/top-langs/?username=GoulartAJG)](https://github.com/GoulartAJG/github-readme-stats)

- Cartão Wakatime

[![estatísticas de wakatime de willianrod](https://github-readme-stats.vercel.app/api/wakatime?username=willianrod)](https://github.com/GoulartAJG/github-readme-stats)

---

### Dica rápida (alinhar os cartões de recompra)

Normalmente, você não poderá dispor as imagens lado a lado. Para fazer isso, você pode usar esta abordagem:

```html
<a href="https://github.com/GoulartAJG/github-readme-stats">
  <img align="center" src="https://github-readme-stats.vercel.app/api/pin/?username=GoulartAJG&repo=github-readme-stats" />
</a>
<a href="https://github.com/GoulartAJG/convoychat">
  <img align="center" src="https://github-readme-stats.vercel.app/api/pin/?username=GoulartAJG&repo=convoychat" />
</a>
```

## Implante em sua própria instância Vercel

#### [Confira o tutorial em vídeo passo a passo por @codeSTACKr](https://youtu.be/n6d4KHSKqGk?t=107)

Como a API do GitHub permite apenas 5k solicitações por hora, meu `https://github-readme-stats.vercel.app/api` pode atingir o limitador de taxa. Se você hospedá-lo em seu próprio servidor Vercel, não precisa se preocupar com nada. Clique no botão implantar para começar!

NOTA: Desde [#58](https://github.com/GoulartAJG/github-readme-stats/pull/58) devemos ser capazes de lidar com mais de 5k solicitações e não ter problemas com tempo de inatividade :D

[![Implantar no Vercel](https://vercel.com/button)](https://vercel.com/import/project?template=https://github.com/GoulartAJG/github-readme-stats)

<detalhes>
 <summary><b> Guia para configurar o Vercel 🔨 </b></summary>

1. Acesse [vercel.com](https://vercel.com/)
1. Clique em 'Login'
   ![](https://files.catbox.moe/tct1wg.png)
1. Faça login no GitHub pressionando 'Continuar com GitHub'
   ![](https://files.catbox.moe/btd78j.jpeg)
1. Faça login no GitHub e permita o acesso a todos os repositórios, se solicitado
1. Fork este repositório
1. Após bifurcar o repositório, abra o arquivo [`vercel.json`](https://github.com/GoulartAJG/github-readme-stats/blob/master/vercel.json#L5) e altere o arquivo `maxDuration` campo para `10`
1. Volte ao seu [painel Vercel](https://vercel.com/dashboard)
1. Selecione "Importar projeto"
   ![](https://files.catbox.moe/qckos0.png)
1. Selecione `Importar repositório Git`. Selecione root e mantenha tudo como está.
   ![](https://files.catbox.moe/pqub9q.png)
1. Crie um token de acesso pessoal (PAT) [aqui](https://github.com/settings/tokens/new) e ative as permissões de `repo` (isso permite o acesso para ver as estatísticas do repositório privado)
1. Adicione o PAT como uma variável de ambiente chamada `PAT_1` (como mostrado).
   ![](https://files.catbox.moe/0ez4g7.png)
1. Clique em implantar e pronto. Veja seus domínios para usar a API!

</detalhes>

## :sparkling_heart: Apoie o projeto

Eu abro quase tudo o que posso e tento responder a todos que precisam de ajuda usando esses projetos. Obviamente,
isso leva tempo. Você pode usar este serviço gratuitamente.

No entanto, se você estiver usando este projeto e estiver satisfeito com ele ou apenas quiser me incentivar a continuar criando coisas, existem algumas maneiras de fazer isso: -

- Dando o devido crédito quando você usa github-readme-stats no seu readme, linkando de volta para ele :D
- Estrelando e compartilhando o projeto :rocket:
- [![paypal.me/GoulartAJG](https://ionicabizau.github.io/badges/paypal.svg)](https://www.paypal.me/GoulartAJG) - Você pode fazer doações únicas via PayPal. Provavelmente vou comprar um ~~café~~ chá. :chá:

Obrigado! :coração:

---

[![https://vercel.com?utm_source=github_readme_stats_team&utm_campaign=oss](./powered-by-vercel.svg)](https://vercel.com?utm_source=github_readme_stats_team&utm_campaign=oss)


Contribuições são bem-vindas! <3

Feito com :heart: e JavaScript.
