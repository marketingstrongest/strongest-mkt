# Configuração do Martin Atendimento (Martz) — Strongest Supplements

Material pronto para colar na Martz, montado a partir do site strongest.com.br e da documentação da Martz.

## Como os produtos ficam automáticos

| Onde | O que entra | Muda quando entra produto novo? |
|---|---|---|
| **Catálogo** (tools Busca + Detalhe do produto) | Todos os produtos: preço, sabores, descrição, modo de uso — lidos da Shopify | **Não.** Automático |
| **Base de Conhecimento** | Só o que vale para a loja toda: políticas, pagamento, cashback, cupons, laudos, marca | Não |
| **Prompts** | Regras e matriz por objetivo/tipo de produto, sem nome nem preço | Não (só se surgir uma linha nova de produto) |
| **Cross-sell** | Correlações por produto + correlação automática por histórico de compras | Só ligar o produto novo à linha dele (opcional) |

## Ordem de configuração (recomendada pela Martz)

1. `01-geral-e-system-prompt.md` → aba **Geral** + **System prompt**
2. `base-de-conhecimento/` → um artigo por arquivo, categoria = nome da pasta, **publicar** todos
3. `02-sub-agente-base-de-conhecimento.md`
4. `03-sub-agente-catalogo.md` (+ ajuste de tags na Shopify)
5. `04-sub-agente-cross-sell.md`
6. `05-sub-agente-pedidos.md`
7. `06-escalacao-e-handover.md`
8. Validar em **Copiloto** (ou Autônomo num setor de teste) antes de liberar o Autônomo

## Decisões confirmadas

- Trocas: a IA informa os prazos (7 dias arrependimento / 90 dias defeito), mas todo pedido de troca/devolução vai para o SAC.
- ANA10: 10% de desconto, sem validade e sem valor mínimo.
- Apenas um cupom por pedido (PRIMEIRACOMPRA, ANA10 ou cashback não acumulam).
- Boleto: desativado (removido dos prompts e da base).
- Desconto progressivo: não existe mais (removido da persona, dos prompts e da base).
- "Whey" é como o cliente chama qualquer proteína em pó: a IA entende e oferece a tradicional ou a vegetal (Future Protein, sem lactose).
- Status de pagamento: tool ligada no sub-agente Pedidos.
- Correlações de cross-sell e mensagem de aviso ao escalar: aprovadas como estão.

## Avisos importantes

- **Tudo o que mudar na Shopify está na página [Ajustes na Shopify](https://claude.ai/artifact/Vo7rLxcRGGFeBJs3qY8ynB)**: variantes, tipo e tags dos 40 produtos, tema, Prime Card e coleções.

- **No site, tire o boleto** das formas de pagamento do rodapé.
- **Na Shopify, tire as variantes "Compre 1 / Compre 2 / Compre 3 … OFF"** do Strong Zen Gotas, Strong Flex, Vitamina C + Zinco e Strong B+. Elas ainda estão no ar e a IA lê essas variantes no Catálogo.
- **No site, troque também o WhatsApp +1 (555) 743-4450** no rodapé e na página de Contato, e ajuste o horário da página de Contato para 8h às 17h. Hoje está 9h às 18h, e a Martz recomenda que o site não contradiga a Fonte da Verdade.
- **Na Shopify, coloque no Future Protein as tags** `whey vegano`, `whey vegetal`, `proteina vegetal`, `vegano`, `sem lactose`, para a busca achar o produto quando o cliente pedir "whey vegano" ou "whey sem lactose".
