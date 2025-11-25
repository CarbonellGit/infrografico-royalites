# Infográfico - Navegando com Sabedoria Digital

Resumo
-	Este repositório contém um único arquivo `index.html` que serve como um folheto/infográfico digital (estático) chamado "Navegando com Sabedoria Digital" criado para o Colégio Carbonell.
-	O projeto usa Tailwind (via CDN) para estilos utilitários e Lucide Icons para ícones.

Arquivos importantes
-	`index.html` — a página principal/única do projeto.
-	`logo.png` — (opcional, não versionado aqui) o logotipo esperado na raiz do projeto; referenciado no cabeçalho com `src="logo.png"`.

Como visualizar localmente
-	Opção 1 — Abrir direto no navegador:
	- Abra o arquivo `index.html` com duplo-clique (gera um caminho `file://`). Funciona para visualização simples, porém alguns recursos CORS ou chamadas dinâmicas podem se comportar diferente.

-	Opção 2 — Servidor HTTP simples (recomendado):
	Se você tiver Python instalado, rode este comando no PowerShell a partir da raiz do projeto:

```powershell
python -m http.server 8000
```

	Depois abra `http://localhost:8000` no navegador.

	Alternativa: instale e use a extensão "Live Server" do VS Code e clique em "Go Live".

Requisitos
-	Navegador moderno (Chrome, Edge, Firefox, Safari).
-	Conexão com internet para carregar Tailwind CDN e Lucide Icons (ou substitua por builds locais se desejar trabalhar offline).

Personalização do logo
-	Coloque o arquivo `logo.png` na raiz do projeto (no mesmo nível de `index.html`).
-	O `index.html` já referencia `logo.png` na tag:

```html
<img src="logo.png" alt="Colégio Carbonell" class="site-logo w-14 h-14 object-contain rounded-md">
```

-	Alterar tamanho/estilo
	- Para aumentar/diminuir, ajuste as classes Tailwind `w-14 h-14` para outra (ex.: `w-20 h-20` ou `w-10 h-10`).
	- Para responsividade mais fina, use classes responsivas, por exemplo:

```html
<img src="logo.png" alt="Colégio Carbonell" class="site-logo w-10 h-10 md:w-16 md:h-16 lg:w-20 lg:h-20 object-contain rounded-md">
```

-	Se preferir estilizar via CSS, edite ou adicione regras para a classe `.site-logo` no próprio arquivo `index.html` ou em um CSS externo.

Sobre Tailwind e Lucide
-	Tailwind é carregado via `https://cdn.tailwindcss.com` no `index.html` — rápido para protótipos.
-	Lucide Icons é carregado via `https://unpkg.com/lucide@latest` e inicializado ao final do `body` com `lucide.createIcons();`.

Dicas e observações
-	Verifique se `logo.png` existe na raiz; se estiver dentro de outra pasta (ex.: `assets/`), atualize o `src` para `assets/logo.png`.
-	Se preferir otimizar para produção, exporte um CSS Tailwind compilado e remova o CDN.
-	Teste em dispositivos móveis para confirmar o espaçamento entre logo e título; ajuste `gap-3` na div do cabeçalho se precisar de mais/menos espaço.

Licença
-	Nenhuma licença foi definida neste repositório. Adicione um arquivo `LICENSE` se desejar explicitar termos de uso.

Contato
-	Se quiser, posso ajustar o posicionamento ou a responsividade do logo — diga qual tamanho/estilo prefere.
