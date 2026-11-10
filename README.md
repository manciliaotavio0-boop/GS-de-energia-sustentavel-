# Citizen Assist AI — Módulo de Energia para Idosos

**Disciplina:** Soluções em Energias Renováveis e Sustentáveis — Global Solution 2026.2 (Ciência da Computação, 1º ano)

## Integrantes
| Nome | RM |
|---|---|
| Tiago Muhlmann | 569569 |
| Wesley Marques | 573915 |
| Otávio Mancilia | 570225 |

## Público e problema
**Público:** idosos que vivem em residência urbana, e familiares ou cuidadores que os ajudam.

**Necessidade:** reduzir a conta de luz sem perder conforto e sem comprometer equipamentos de saúde (como concentrador de oxigênio ou CPAP). Idosos costumam passar mais tempo em casa, ter renda fixa e usar chuveiro elétrico quente, o que pesa no orçamento. Também são alvo frequente de golpes na venda de painéis solares.

**Como as orientações ajudam:** o assistente mostra onde a casa gasta mais, compara duas alternativas com custo, retorno e impacto ambiental, e alerta sobre golpes e sobre não reduzir equipamentos de saúde.

## Funcionalidades de energia
Assistente em menu dentro do notebook:
1. Consumo de uma casa de exemplo (kWh e R$ por equipamento)
2. Comparação entre as alternativas A e B
3. Cálculo com a tarifa de luz do próprio usuário
4. Avisos de saúde, golpes e limitações
5. Fontes e referências

O assistente trata entradas inválidas e não coleta dados pessoais. Não é um canal oficial de distribuidora ou órgão público.

## Alternativas comparadas (período de referência: 10 anos)
- **A — Economia:** trocar lâmpadas incandescentes por LED e a geladeira antiga por uma com selo Procel A.
- **B — Fonte renovável:** aquecedor solar de água, substituindo parte do consumo do chuveiro elétrico.

**Resultado com os dados atuais (estimado):**
- A: investimento de cerca de R$ 2.572, retorno em cerca de 2,4 anos.
- B: investimento de cerca de R$ 5.000, retorno em cerca de 7,5 anos.
- O CO₂ evitado é baixo nas duas, porque a matriz elétrica brasileira já é majoritariamente renovável. O ganho principal é financeiro.

  
## Dados e premissas
Todos ficam na seção 1 do notebook, com origem comentada no código. Resumo:

| Dado | Valor | Origem |
|---|---|---|
| Tarifa | R$ 1,10/kWh (calculado) | ANEEL, InfoTarifas, jun/2026 (via Poder360) |
| Fator de CO₂ | 0,0385 kg/kWh | MCTI, média anual do SIN 2023 |
| Geladeira antiga / Procel A | 70 / 35 kWh/mês | Revista Oeste, Monitor do Mercado (2026) |
| Aquecedor solar | R$ 5.000 | Monitor do Mercado (2026) |
| Potências, horas de uso, preços de LED e geladeira nova, fração solar de 70% | — | **ESTIMADO** (premissas do grupo) |

## Cálculos
- Energia (kWh/mês) = potência (kW) × horas por dia × 30 dias
- Custo mensal = kWh × tarifa
- Economia anual = (kWh antes − kWh depois) × 12 × tarifa − manutenção
- Payback (anos) = investimento ÷ economia anual
- CO₂ evitado = kWh evitados × 12 × fator de emissão

Simplificações: sem juros, sem inflação da tarifa, sem bandeiras tarifárias e sem degradação dos equipamentos.

## Justificativa das recomendações
- **Custos:** LED tem retorno rápido. A geladeira e o aquecedor solar exigem mais investimento e retornam mais devagar.
- **Viabilidade:** o aquecedor solar precisa de telhado ou laje com sol e espaço para o reservatório, e pode não servir para apartamento ou imóvel alugado. LED e geladeira servem para qualquer moradia.
- **Impacto ambiental:** o CO₂ evitado por kWh é baixo no Brasil. O benefício ambiental existe, mas é modesto.
- **Ordem sugerida:** começar pelo LED e avaliar o solar se houver telhado adequado e orçamento.
- **Saúde:** nenhuma recomendação reduz o uso de equipamentos de saúde.

## Limitações
Os valores são estimativas e não garantem economia. Tarifa, custos, consumo dos aparelhos e fração solar variam por casa, região e época. Os custos do aquecedor solar variam muito (R$ 5 mil a mais de R$ 15 mil). O assistente não substitui orçamentos reais nem orientação de um profissional.

## Como executar
1. Abra https://colab.research.google.com
2. **Arquivo > Fazer upload de notebook** e escolha `citizen_assist_energia.ipynb`
3. **Ambiente de execução > Executar tudo**
4. Na célula do assistente, digite o número da opção e pressione Enter. Digite `0` para sair.


## Referencias:
- ANEEL, boletim InfoTarifas (via Poder360): https://poder360.com.br/poder-infra/aneel-projeta-alta-de-86-na-conta-de-luz-em-2026
- MCTI, fator de emissão do SIN 2023: https://www.gov.br/mcti/pt-br/acompanhe-o-mcti/noticias/2024/02/fator-de-emissao-de-co2-na-geracao-de-energia-eletrica-no-brasil-em-2023-e-o-menor-em-12-anos
- MCTI/SIRENE, fatores mensais 2025 (via Canal Solar): https://canalsolar.com.br/emissoes-de-co%e2%82%82-geracao-eletrica-mcti/
- Consumo de geladeiras, Revista Oeste: https://revistaoeste.com/oestegeral/?p=85762
- Procel/Idec, consumo de eletrodomésticos: https://idec.org.br/print/24463
- Custo de aquecimento solar 2026, Monitor do Mercado: https://monitordomercado.com.br/economia-2/406364-quanto-custa-instalar-aquecimento-solar-de-agua-e-reduzir-o-uso-do-chuveiro-eletrico/
- Procel/Inmetro, etiqueta ENCE e tabelas PBE: https://www.gov.br/inmetro
- ANEEL, tarifas e Tarifa Social: https://www.gov.br/aneel

## Vídeo
`[PREENCHER: link do vídeo não listado no YouTube]`
