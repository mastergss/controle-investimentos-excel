Planilha automatizada para gestão de carteira e acompanhamento de dividendos

# 📈 Simulador de Investimentos em Fundos Imobiliários (FIIs)
Ferramenta desenvolvida do zero no Microsoft Excel para simular a evolução patrimonial e a geração de renda passiva (dividendos) através de aportes mensais em Fundos Imobiliários.

---

## 🎯 Descrição do Projeto
O projeto consiste na criação de um simulador financeiro completo partindo de uma planilha em branco (sem base de dados prévia), estruturado em **5 etapas práticas** até chegar a uma planilha final que servirá como **Gabarito**.

Este repositório reúne:
* A planilha finalizada (`.xlsx`).
* O Simulador de Investimentos interativo.
* Prints das telas e resultados.
* O detalhamento lógico de cada cálculo realizado.

---

## ❓ Perguntas de Negócio Respondidas
A ferramenta foi desenhada para responder aos seguintes questionamentos do investidor:
* **Valor do Aporte:** Quanto devo investir (R$) por mês?
* **Horizonte de Tempo:** Qual o tempo de investimento (em meses e anos)?
* **Rentabilidade:** Quais são as taxas de rendimentos mensais e anuais aplicadas?
* **Acúmulo de Capital:** Qual será o patrimônio acumulado ao final do período?
* **Renda Passiva:** Quais serão os dividendos mensais gerados pelo patrimônio?

---

## ⚙️ Funcionalidades e Recursos do Excel
Para tornar o simulador dinâmico e à prova de erros, foram aplicados os seguintes recursos:
* **Projeção de Longo Prazo:** Simulação de cenários de **2 a 30 anos**.
* **Cálculo de Patrimônio:** Uso da função financeira **`VF` (Valor Futuro)** para projetar aportes mensais e reinvestimento.
* **Perfil de Investidor:** Divisão estratégica de aportes baseada no perfil selecionado.
* **Busca Dinâmica:** Integração de **`PROCV`** associada a uma **Tabela de Apoio** para automatizar parâmetros.
* **Organização de Fórmulas:** Uso de **Intervalos Nomeados** para facilitar a leitura e manutenção dos cálculos.

---

## 🧮 Detalhes dos Cálculos (Etapa Atual)
Nesta primeira versão do simulador, o foco está na projeção do acúmulo de capital ao longo do tempo utilizando a função financeira **Valor Futuro (`VF`)**.

### Projeção de Patrimônio Acumulado (`VF`)
A função `VF` calcula o montante total acumulado ao final do período escolhido, considerando os juros compostos sobre o capital inicial e os aportes mensais constantes.

* **Fórmula utilizada:**
  ```excel
  =VF(taxa; nper; pgto; [vp]; [tipo])
  ```
* **Exemplo aplicado na planilha:**
  ```excel
  =VF(Taxa_Mensal; Prazo_Meses; -Aporte_Mensal; -Patrimonio_Inicial; 0)
  ```

* **Explicação de cada argumento:**
  * **`taxa` (Taxa Mensal):** Rentabilidade percentual aplicada a cada mês.
  * **`nper` (Número de Períodos):** Total de meses da simulação (ex: para 10 anos, `120` meses).
  * **`pgto` (Pagamento/Aporte):** Valor investido mensalmente. *Nota: Inserido com sinal negativo (`-`) por convenção de fluxo de caixa do Excel (saída do bolso para o investimento), garantindo que o resultado final apareça positivo.*
  * **`[vp]` (Valor Presente):** Patrimônio inicial já acumulado antes de iniciar os novos aportes (também com sinal negativo, ou `0` se começar do zero).
  * **`[tipo]`:** Definido como `0` (ou omitido), indicando que os aportes são realizados ao final de cada mês.

--- 

## 🖼️ Prévia do Projeto
*(Espaço reservado para você adicionar os prints da sua planilha depois de criá-la)*

---

## 🚀 Como Utilizar
1. Clique no arquivo `.xlsx` disponível neste repositório e faça o download (**View raw** / **Download**).
2. Abra o arquivo no Microsoft Excel.
3. Preencha os parâmetros de entrada (valor do aporte, perfil e prazo) para visualizar a projeção de patrimônio e dividendos.
