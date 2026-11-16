# 📈 ROI e Payback de Automação com IA

**🔗 Demo ao vivo: https://moniquesilva79.github.io/roi-automacao-ia/**

Calcula se um projeto de automação com IA ou RPA se paga, e em quanto tempo. Considera a **rampa de adoção**, já que a economia não vem completa no primeiro mês, e entrega **payback, VPL, TIR e ROI** no horizonte escolhido, com o fluxo de caixa acumulado mês a mês.

## 🎯 Problema que resolve
Todo business case de IA precisa responder a três perguntas do CFO: quanto vou investir, quando recupero o dinheiro e quanto ganho no final. Planilhas costumam ignorar a rampa de adoção e o custo recorrente de operar a IA, o que gera promessas otimistas demais.

## ✨ Funcionalidades
- Investimento inicial, custo recorrente, custo atual do processo, percentual de redução e outros ganhos mensuráveis
- Rampa de adoção linear até a economia plena
- Payback em meses, VPL com taxa de desconto anual, TIR anualizada e ROI no horizonte
- Gráfico do fluxo de caixa acumulado com o ponto de payback
- Resumo por ano e diagnóstico automático (viável, VPL negativo ou nunca se paga)

## 🧮 Como o cálculo funciona
```
benefício(t) = (custo atual × redução + outros ganhos) × min(t ÷ meses de rampa, 1)
fluxo(t)     = benefício(t) − custo recorrente;  fluxo(0) = − investimento inicial
payback      = primeiro mês com fluxo acumulado ≥ 0
VPL          = Σ fluxo(t) ÷ (1 + i)^t,  com i = (1 + taxa anual)^(1/12) − 1
TIR          = taxa i que zera o VPL (bisseção), anualizada
ROI          = (benefícios − custos) ÷ custos no horizonte
```

## 📊 Exemplo (valores padrão)
| Indicador | Valor |
|---|---|
| Investimento inicial | R$ 250.000 |
| Economia plena | R$ 62.000/mês (45% de R$ 120 mil + R$ 8 mil) |
| Custo recorrente | R$ 18.000/mês |
| Payback | **10 meses** |
| ROI em 36 meses | 131,3% |
| VPL a 12% ao ano | R$ 934.857 |

## 🧰 Tecnologias
HTML, CSS e JavaScript puros, sem frameworks, sem dependências e sem servidor. Publicado no GitHub Pages.

## 🚀 Como rodar localmente
```bash
git clone https://github.com/MoniqueSilva79/roi-automacao-ia.git
cd roi-automacao-ia
python -m http.server 8000   # e acesse http://localhost:8000
```

## ⚠️ Limitações
Os valores padrão são ilustrativos. O modelo não considera impostos sobre o resultado, depreciação nem inflação dos custos. Use como apoio ao business case, validado com a área financeira.

## 🗺️ Próximos passos
- [ ] Cenários pessimista, base e otimista
- [ ] Rampa em curva S
- [ ] Exportar o business case em PDF

## 🔗 Série de calculadoras de IA
[Custo por tarefa de agentes](https://moniquesilva79.github.io/custo-agentes-ia/) · [Precificação do FTE digital](https://moniquesilva79.github.io/precificacao-fte-digital/) · [ROI e payback](https://moniquesilva79.github.io/roi-automacao-ia/) · [Priorização de processos](https://moniquesilva79.github.io/priorizacao-processos/) · [Revisão humana x custo do erro](https://moniquesilva79.github.io/revisao-humana-ia/) · [Curva de melhoria contínua](https://moniquesilva79.github.io/curva-melhoria-ia/)

---
Projeto autoral de **Monique da Silva Cruz**: [LinkedIn](https://www.linkedin.com/in/moniquesilva-cloud-ti-projetos-latam) · [outros projetos](https://github.com/MoniqueSilva79)
