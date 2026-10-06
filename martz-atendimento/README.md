# Configuração do Martin Atendimento (Martz) — Strongest Supplements

Material pronto para colar na Martz, montado a partir do site strongest.com.br e da documentação da Martz.

## Como os produtos ficam automáticos

| Onde | O que entra | Muda quando entra produto novo? |
|---|---|---|
| **Catálogo** (tools Busca + Detalhe do produto) | Todos os produtos: preço, sabores, descrição, modo de uso — lidos da Shopify | **Não.** Automático |
| **Base de Conhecimento** | Só o que vale para a loja toda: políticas, pagamento, cashback, cupons, laudos, marca | Não |
| **Prompts** | Regras e matriz por objetivo/tipo de produto, sem nome nem preço | Não (só se surgir uma linha nova, ex.: proteína vegetal) |
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

## Pendências — preciso da sua confirmação

1. **Prazos de troca na Fonte da Verdade.** Na pergunta 3 você liberou as regras de 7 dias (arrependimento) e 90 dias (defeito), mas o seu System prompt dizia "não informar prazo, escalar". Deixei assim: **a IA informa os prazos, mas qualquer pedido de troca/devolução vai para o SAC.** Se preferir que ela nem fale os prazos, é preciso tirar os artigos `devolucao-por-arrependimento.md` e `garantia-e-defeito-de-fabricacao.md`, senão eles contradizem a Fonte da Verdade.
2. **ANA10:** qual o % de desconto? Vale na primeira compra junto com o PRIMEIRACOMPRA? Tem validade ou valor mínimo?
3. **Boleto:** aparece como forma de pagamento no rodapé do site, mas não está na sua Fonte da Verdade. Está ativo?
4. **Status de pagamento (sub-agente Pedidos):** quer que a IA ajude o cliente com Pix ou pagamento pendente?
5. **Correlações de cross-sell:** a tabela em `04-sub-agente-cross-sell.md` é uma sugestão minha a partir dos kits do site. Revise antes de cadastrar.
6. **Mensagem de aviso ao escalar:** o texto em `06-escalacao-e-handover.md` é uma sugestão.

## Avisos importantes

- **No site, troque também o WhatsApp +1 (555) 743-4450** no rodapé e na página de Contato, e ajuste o horário da página de Contato para 8h às 17h. Hoje está 9h às 18h, e a Martz recomenda que o site não contradiga a Fonte da Verdade.
- Tirei o exemplo "whey vegetal e sem lactose" da persona porque **não existe esse produto no catálogo**. Se lançarem, é só voltar o exemplo.
