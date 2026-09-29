# Produtos e Inventário

> Listagem, ordenação, detalhe e adição de itens

**URL sob teste:** https://www.saucedemo.com/  
**Total de casos:** 23

Legenda de status: ⬜ Não executado · ✅ Passou · ❌ Falhou · ⚠️ Bloqueado

| ID | Título | Pré-condições | Passos | Resultado esperado | Prioridade | Status |
|----|--------|---------------|--------|--------------------|:----------:|:------:|
| PRD-001 | Listagem exibe os 6 produtos | Logado como `standard_user` (senha `secret_sauce`) na tela de produtos | 1. Observar a tela de produtos | 6 produtos, cada um com imagem, nome, descrição, preço e botão "Add to cart" | Alta | ⬜ |
| PRD-002 | Nomes e preços corretos | Logado como `standard_user` (senha `secret_sauce`) na tela de produtos | 1. Conferir cada item da lista | Backpack $29.99, Bike Light $9.99, Bolt T-Shirt $15.99, Fleece Jacket $49.99, Onesie $7.99, Test.allTheThings() T-Shirt (Red) $15.99 | Alta | ⬜ |
| PRD-003 | Ordenação padrão | Logado como `standard_user` (senha `secret_sauce`) na tela de produtos | 1. Observar o seletor de ordenação ao carregar a tela | Opção "Name (A to Z)" selecionada; lista em ordem alfabética crescente | Média | ⬜ |
| PRD-004 | Ordenar por nome Z a A | Logado como `standard_user` (senha `secret_sauce`) na tela de produtos | 1. Selecionar "Name (Z to A)" | Lista em ordem alfabética decrescente (Test.allTheThings() primeiro, Backpack por último) | Alta | ⬜ |
| PRD-005 | Ordenar por preço do menor ao maior | Logado como `standard_user` (senha `secret_sauce`) na tela de produtos | 1. Selecionar "Price (low to high)" | Ordem: Onesie, Bike Light, itens de $15.99, Backpack, Fleece Jacket | Alta | ⬜ |
| PRD-006 | Ordenar por preço do maior ao menor | Logado como `standard_user` (senha `secret_sauce`) na tela de produtos | 1. Selecionar "Price (high to low)" | Ordem: Fleece Jacket, Backpack, itens de $15.99, Bike Light, Onesie | Alta | ⬜ |
| PRD-007 | Adicionar um produto ao carrinho | Logado como `standard_user` (senha `secret_sauce`) na tela de produtos | 1. Clicar em "Add to cart" no Backpack | Botão vira "Remove" e o ícone do carrinho mostra o número 1 | Alta | ⬜ |
| PRD-008 | Adicionar vários produtos | Logado como `standard_user` (senha `secret_sauce`) na tela de produtos | 1. Adicionar Backpack, Bike Light e Onesie | Os três botões viram "Remove" e o contador do carrinho mostra 3 | Alta | ⬜ |
| PRD-009 | Remover produto na listagem | Logado como `standard_user` (senha `secret_sauce`) na tela de produtos | 1. Adicionar 2 produtos<br>2. Clicar em "Remove" em um deles | Botão volta a "Add to cart" e o contador cai para 1. Ao remover o último, o contador desaparece | Alta | ⬜ |
| PRD-010 | Abrir detalhe pelo nome | Logado como `standard_user` (senha `secret_sauce`) na tela de produtos | 1. Clicar no nome "Sauce Labs Backpack" | Abre `/inventory-item.html?id=4` com o detalhe do produto | Média | ⬜ |
| PRD-011 | Abrir detalhe pela imagem | Logado como `standard_user` (senha `secret_sauce`) na tela de produtos | 1. Clicar na imagem do Backpack | Abre a mesma página de detalhe do produto | Média | ⬜ |
| PRD-012 | Conteúdo da página de detalhe | Logado como `standard_user` (senha `secret_sauce`) na tela de produtos | 1. Abrir o detalhe de qualquer produto | Imagem, nome, descrição completa, preço, botão de carrinho e "Back to products" corretos e coerentes com a listagem | Média | ⬜ |
| PRD-013 | Adicionar e remover no detalhe | Logado como `standard_user` (senha `secret_sauce`) na tela de produtos | 1. Abrir detalhe<br>2. Clicar em "Add to cart"<br>3. Clicar em "Remove" | Botão alterna corretamente e o contador do carrinho acompanha | Alta | ⬜ |
| PRD-014 | Botão Back to products | Logado como `standard_user` (senha `secret_sauce`) na tela de produtos | 1. Abrir detalhe<br>2. Clicar em "Back to products" | Retorna a `/inventory.html` | Média | ⬜ |
| PRD-015 | Detalhe com id inexistente | Logado como `standard_user` (senha `secret_sauce`) na tela de produtos | 1. Acessar `/inventory-item.html?id=999` | Sistema trata o caso com mensagem ou tela adequada, sem quebrar. A confirmar comportamento real | Baixa | ⬜ |
| PRD-016 | Estado do botão consistente entre telas | Logado como `standard_user` (senha `secret_sauce`) na tela de produtos | 1. Adicionar item na listagem<br>2. Abrir o detalhe desse item | No detalhe o botão já aparece como "Remove" | Média | ⬜ |
| PRD-017 | Ordenação preserva itens no carrinho | Logado como `standard_user` (senha `secret_sauce`) na tela de produtos | 1. Adicionar Backpack<br>2. Trocar a ordenação | Backpack continua com "Remove" na nova posição e o contador é mantido | Média | ⬜ |
| PRD-018 | Estado do carrinho após recarregar | Logado como `standard_user` (senha `secret_sauce`) na tela de produtos | 1. Adicionar 2 itens<br>2. Pressionar F5 | Contador e botões "Remove" permanecem | Média | ⬜ |
| PRD-019 | Links do rodapé | Logado como `standard_user` (senha `secret_sauce`) na tela de produtos | 1. Clicar em Twitter, Facebook e LinkedIn no rodapé | Cada link abre a página oficial do Sauce Labs em nova aba; texto de copyright presente | Baixa | ⬜ |
| PRD-020 | problem_user: imagens dos produtos | Navegador aberto em https://www.saucedemo.com/ com usuário deslogado | 1. Logar com `problem_user`<br>2. Observar as imagens | Cada produto deve ter sua própria imagem. Obs.: neste usuário a demo exibe a mesma imagem em todos (defeito proposital, útil para detectar regressão) | Média | ⬜ |
| PRD-021 | problem_user: ordenação | Navegador aberto em https://www.saucedemo.com/ com usuário deslogado | 1. Logar com `problem_user`<br>2. Trocar a ordenação | Lista deve ser reordenada. Obs.: a demo pode não reordenar (defeito proposital). A confirmar | Média | ⬜ |
| PRD-022 | problem_user: adicionar e remover itens | Navegador aberto em https://www.saucedemo.com/ com usuário deslogado | 1. Logar com `problem_user`<br>2. Adicionar e remover vários itens | Todos os botões devem funcionar. Obs.: alguns podem falhar (defeito proposital). A confirmar quais | Média | ⬜ |
| PRD-023 | visual_user: layout | Navegador aberto em https://www.saucedemo.com/ com usuário deslogado | 1. Logar com `visual_user`<br>2. Comparar a tela com a do `standard_user` | Layout deve ser idêntico. Obs.: a demo insere divergências visuais (posição, alinhamento). Registrar diferenças | Baixa | ⬜ |
