# analise-funil-teste-aab
📱 Análise de Funil e Teste A/A/B — App de Produtos Alimentícios

📌 Sobre o Projeto

Projeto de análise comportamental desenvolvido para uma startup do setor alimentício. O objetivo foi estudar o funil de vendas do aplicativo e avaliar o impacto de uma mudança de design (fonte) no comportamento dos usuários através de um experimento A/A/B.

O dataset contém mais de 244 mil eventos registrados por 7.551 usuários únicos, cobrindo o período de agosto de 2019.

🔍 Parte 1 — Análise do Funil de Vendas

Etapas do funil

EtapaUsuáriosConversão🏠 Tela Principal (MainScreenAppear)7.41998,47%🛍️ Tela de Ofertas (OffersScreenAppear)4.59360,96%🛒 Carrinho (CartScreenAppear)3.73449,56%✅ Pagamento concluído (PaymentScreenSuccessful)3.53946,97%

Perda entre etapas

TransiçãoPerdaTela Principal → Ofertas⚠️ 38,09% — maior gargaloOfertas → Carrinho18,70%Carrinho → Pagamento5,22%

Conclusão

47,7% dos usuários que acessam o app completam o pagamento
O maior gargalo está na transição da tela principal para as ofertas — foco prioritário de melhoria
Quem chega ao carrinho tem alta intenção de compra (apenas 5,2% de abandono)

🧪 Parte 2 — Experimento A/A/B (Teste de Fonte)

Configuração do experimento

GrupoTipoUsuários246Controle A (fonte antiga)2.484247Controle B (fonte antiga)2.513248Teste (nova fonte)2.537

Validação A/A (Grupos 246 vs 247)

Todos os eventos com p-valor > 0,05 — grupos equivalentes ✅
Confirma que a divisão dos usuários foi feita corretamente.

Resultados A/B (Controle combinado vs Grupo 248)

EventoControleTestep-valorResultadoMainScreenAppear98,58%98,27%0,2942Sem diferença ✅OffersScreenAppear61,28%60,35%0,4343Sem diferença ✅CartScreenAppear50,11%48,48%0,1818Sem diferença ✅PaymentScreenSuccessful47,19%46,55%0,6004Sem diferença ✅Tutorial11,23%11,00%0,7649Sem diferença ✅

Correção de Bonferroni

Com 20 testes realizados, o alpha corrigido foi de 0,0025. Mesmo com essa correção mais rigorosa, nenhum resultado foi significativo — a conclusão é robusta.

Conclusão

A mudança de fonte pode ser implementada com segurança. O medo dos gerentes de que o novo design fosse intimidador não foi confirmado pelos dados.

🛠️ Ferramentas Utilizadas

Python — análise e tratamento dos dados
Pandas / NumPy — manipulação do dataset
Plotly — visualizações interativas (funil, gráfico de barras)
SciPy / Statsmodels — teste de proporções (proportions_ztest)
Jupyter Notebook — ambiente de desenvolvimento

📁 Estrutura do Repositório

📦 analise-funil-teste-aab
 ┣ 📓 Testes.ipynb     → Notebook completo com análise
 ┗ 📝 README.md        → Documentação do projeto


👨‍💻 Autor

Raphael Victor
Estudante de Data Analytics | TripleTen
