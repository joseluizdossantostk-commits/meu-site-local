# Registro de decisões — Guia de Locais e Eventos (Suzano)

## Escopo
A atualização foi feita sobre o guia existente, preservando o conteúdo e a identidade visual azul e branca. O CSS comum foi movido para `css/style.css`.

## Tipografia fluida — contas dos extremos
Regra usada nos títulos principais: `clamp(1.8rem, 4vw, 3.5rem)`.
Considerando `1rem = 16px`:
- Em 360px: 4vw = 14,4px; o mínimo de 1,8rem = 28,8px prevalece.
- Em 1280px: 4vw = 51,2px; o máximo de 3,5rem = 56px não é atingido, então o valor preferido (51,2px) prevalece.
Observação: a conta acima considera a largura da viewport e o tamanho-base padrão de 16px.

## Registro por página

### `ex,8.html` — Home
| CSS compartilhado resolveu | Específico da página |
|---|---|
| Reset de box-sizing, fonte, cores e layout geral | `clamp()` aplicado ao título “Descubra sua cidade” |
| Regra universal de mídia responsiva | Cards organizados em Grid e conteúdo de locais |
| Links com área mínima de toque e foco visível | Seções Eventos e Contato receberam conteúdo informativo em vez de âncoras vazias |
| Breakpoint de layout para telas maiores | Âncoras de categorias ligadas aos cards correspondentes |

### `detalhe.html` — Parque Max Feffer
| CSS compartilhado resolveu | Específico da página |
|---|---|
| Cabeçalho, navegação, cores, tipografia-base e rodapé | Título “Parque Max Feffer” com `clamp()` |
| Área de toque e foco visível | Navegação lateral para apresentação, sobre e atividades |
| Regra universal de mídia e comportamento responsivo | Links corrigidos para apontar para `ex,8.html` |

## Auditoria Lighthouse — preencher após executar no Chrome
A pontuação não foi presumida nem simulada. Execute Lighthouse > Accessibility separadamente em cada página e registre abaixo os dados reais.

### Home (`ex,8.html`)
- Nota de acessibilidade: deu 17/18_eu acho q seria 90 ou 95 / 100 (meta: 90 ou mais)
- Achado concreto do relatório:Contraste entre texto e fundo insuficiente em alguns elementos.
- Elemento/localização: Elementos de texto da página, identificados pelo Lighthouse na verificação de contraste.
- Correção aplicada ou justificativa para discordar: Não corrigido nesta etapa. O Lighthouse identificou uma oportunidade de melhoria relacionada ao contraste. A página continua com 17/18 auditorias de acessibilidade aprovadas.

### Parque (`detalhe.html`)
- Nota de acessibilidade: deu 16/17_eu acho q seria 90 ou 95 / 100 (meta: 90 ou mais)
- Achado concreto do relatório: Contraste entre texto e fundo insuficiente.
- Elemento/localização: Texto da página, incluindo elementos dentro do <header class="header"> e da área lateral <aside class="lateral">, conforme apontado pelo Lighthouse.
- Correção aplicada ou justificativa para discordar: Não corrigido nesta etapa. O Lighthouse identificou uma oportunidade de melhoria relacionada ao contraste. A página continua com 16/17 auditorias de acessibilidade aprovadas.

## Verificação manual — marcar somente após testar
- [x] Redimensionei continuamente em 360px, 390px, 768px e 1280px.
- [x] Testei home e detalhe em emulação de aparelho.
- [x] Naveguei com Tab e confirmei foco visível.
- [x] Verifiquei links/botões com área de toque confortável.
- [x] Confirmei ausência de rolagem horizontal indesejada em todas as larguras.
- [x] Rodei Lighthouse nas duas páginas e registrei os resultados reais.

## Entrega
Compactar a pasta `Guia-de-Locais-Suzano` em ZIP junto com este registro.
