# Guia de Contribuição

Obrigado por considerar contribuir com o **Corrida Lendária**! 🏎️

Este é um projeto acadêmico/pessoal, mas contribuições, sugestões e correções são muito bem-vindas.

## Como contribuir

1. Faça um **fork** do repositório
2. Crie uma branch a partir da `main` para a sua alteração:
   ```bash
   git checkout -b feature/nome-da-sua-feature
   ```
3. Instale as dependências e rode o projeto localmente (veja o [README](./README.md))
4. Faça suas alterações
5. Rode o lint e os testes antes de enviar:
   ```bash
   npm run lint
   npm run test
   ```
6. Faça o commit das suas alterações seguindo o padrão abaixo
7. Envie um **Pull Request** para a branch `main`, descrevendo o que foi alterado e por quê

## Padrão de commits

Utilize mensagens de commit curtas e descritivas, preferencialmente seguindo o padrão:

```
tipo: descrição breve da alteração

feat: adiciona nova seção de estatísticas dos pilotos
fix: corrige colisão do carro no jogo
docs: atualiza instruções de instalação no README
style: ajusta espaçamento do NavBar
refactor: separa lógica do jogo em hook customizado
```

Tipos comuns: `feat`, `fix`, `docs`, `style`, `refactor`, `test`, `chore`.

## Reportando problemas (Issues)

Ao abrir uma issue, inclua:

- Descrição clara do problema ou sugestão
- Passos para reproduzir (se for um bug)
- Comportamento esperado x comportamento observado
- Screenshots, se fizer sentido

## Código de conduta

Seja respeitoso(a) e construtivo(a) nas discussões. O objetivo é aprender e evoluir o projeto juntos.
