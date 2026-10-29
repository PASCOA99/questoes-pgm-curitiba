# Questões inéditas PGM Curitiba — GitHub Pages

Site estático, dark glassmorphism, responsivo, **sem conversão para JSON e sem dependências externas**.

## Publicação em seis passos (GitHub no navegador)

1. Entre em https://github.com/new e crie o repositório **questoes-pgm-curitiba** como **Public**. Se a conta for gratuita, Pages requer repositório público.
2. Descompacte o ZIP recebido e abra a pasta `PGM_CURITIBA_GITHUB_PAGES_SITE`.
3. Em seu repositório, clique em **Add file → Upload files**. Arraste **todo o conteúdo** dessa pasta (incluindo `assets` e `bancos`), **não o arquivo ZIP**. Conclua o commit.
4. Vá a **Settings → Pages → Build and deployment**.
5. Em **Source**, selecione **Deploy from a branch**; selecione **main** e **/(root)**; clique em **Save**.
6. O endereço padrão será `https://SEU-USUARIO.github.io/questoes-pgm-curitiba/` (substitua `SEU-USUARIO` pelo usuário do GitHub e ajuste o nome do repositório, se diferente).

## Como atualizar ou inserir um banco — sem alterar o layout

Substitua **apenas o arquivo original** no caminho correspondente do repositório, mantendo nome e pasta:

| Matéria | Arquivo a substituir | Situação inicial |
| --- | --- | --- |
| Administrativo | `bancos/administrativo.html` | Banco original com 870 questões, copiado sem modificações |
| Constitucional | `bancos/constitucional.html` | Página provisória; substitua pelo HTML integral |
| Tributário e Financeiro | `bancos/tributario-financeiro.html` | Página provisória; substitua pelo HTML integral |
| Ambiental e Urbanístico | `bancos/ambiental-urbanistico.html` | Banco original com 403 questões, copiado sem modificações |

Para substituir: clique no arquivo no repositório; use o menu de edição ou exclua o antigo e faça upload do novo mantendo **exatamente o mesmo caminho**. Quando publicar outra versão, o navegador poderá utilizar cache; recarregue com Ctrl+F5 se necessário.

**Não é necessário editar** `index.html`, `assets/site.css`, `assets/site.js` nem as quatro páginas de matéria. O menu fixo continuará funcionando.

## Arquitetura

- `index.html`: página inicial, com título e menu expansível.
- `administrativo.html`, `constitucional.html`, `tributario-financeiro.html`, `ambiental-urbanistico.html`: quatro páginas de matéria com cabeçalho fixo e visualização ampla do HTML original.
- `bancos/*.html`: arquivos originais autônomos, com todas as questões, funções e CSS/JS próprios, exibidos dentro de iframe da mesma origem.
- `assets/site.css`, `assets/site.js`: layout e navegação; nenhuma biblioteca externa.
- `.nojekyll`: impede processamento desnecessário por Jekyll.

## Funcionalidade e privacidade

- O banco original roda **dentro de um iframe da mesma origem**, sem alteração de scripts. Isso conserva os controles existentes, incluindo teclado, comentários, filtros, navegação, estatísticas e armazenamento local quando o navegador permitir.
- O menu superior fica fora do banco e permanece visível.
- O link no cabeçalho **↗ Abrir banco original** permite executar o HTML original sem a moldura, se preferir.
- O progresso é salvo por domínio e navegador. Ao mudar de domínio (por exemplo, do Blogger para GitHub Pages), **o progresso antigo não será transferido automaticamente**. Use exportar/importar progresso quando o banco disponibilizar essas funções.
- O banco de Direito Administrativo e o de Ambiental e Urbanístico utilizam suas respectivas chaves de progresso, conforme seus scripts originais.
- Ao substituir um banco, recomenda-se conservar suas chaves de armazenamento quando quiser manter compatibilidade de progresso.
- Sites publicados no GitHub Pages são públicos. Não inclua informações pessoais, segredos ou dados sensíveis nos arquivos.

## Observações

- Para testar todos os recursos, use o endereço HTTPS publicado no GitHub Pages. Abrir os arquivos por `file://` pode restringir o armazenamento e outros recursos por regras do navegador.
- Na versão desktop e mobile o menu é fixo e o banco rola na área central da tela. Essa rolagem independente é intencional para manter a navegação superior sempre acessível.
- O material é um projeto independente de estudo; não é afiliado à banca FAFIPA ou à Prefeitura de Curitiba.

Referências: https://docs.github.com/pt/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site e https://docs.github.com/pt/repositories/working-with-files/managing-files/adding-a-file-to-a-repository
