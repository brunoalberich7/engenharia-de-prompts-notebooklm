# Engenharia de Prompts com NotebookLM 🚀

> **Projeto Prático - DIO (Digital Innovation One)**  
> **Tema:** Engenharia de Prompts para LLMs  
> **Ferramenta de Aprendizagem:** Google NotebookLM  

---

## 1. Contexto e Objetivos 📌

### Contexto
A Engenharia de Prompts emergiu como uma disciplina essencial na era da IA Generativa, funcionando como uma ponte entre as intenções humanas e a execução das máquinas. Este projeto aplica o uso da Inteligência Artificial como ferramenta de aprendizagem ativa por meio do Google NotebookLM, combinando curadoria de fontes, pensamento crítico e documentação estruturada.

### Objetivos de Estudo
* Compreender os conceitos fundamentais e a arquitetura básica por trás dos prompts (tokenização, vetores e mecanismos de atenção).
* Explorar e testar técnicas estratégicas de estruturação (Zero-shot, Few-shot, Chain-of-Thought, Persona/Papel, Delimitadores).
* Documentar o processo de aprendizado e o comportamento da IA diante de diferentes estruturas de comando (*Troubleshooting*).
* Criar um miniguia prático e reutilizável para apoiar futuras consultas e revisões.

---

## 2. Curadoria de Fontes 📚

Para fundamentar a base de conhecimento deste caderno no **Google NotebookLM**, foram selecionadas e carregadas as seguintes 5 fontes:

1. **The Prompt Canvas (PDF)**: Guia prático baseado na literatura para criação de prompts eficazes em Modelos de Linguagem de Grande Escala (LLMs). *(Artigo: "The Prompt Canvas: A Literature-Based Practitioner Guide for Creating Effective Prompts in Large Language Models")*
2. **Vídeo Explicativo sobre IA / Prompts (YouTube):** Análise prática de conceitos e casos de uso de IA generativa. [Acessar Link](https://www.youtube.com/watch?v=lTI4FyO0ul8)
3. **IBM Think - O que é Engenharia de Prompts:** Artigo conceitual sobre a importância do prompt na otimização de LLMs empresariais. [Acessar Link](https://www.ibm.com/br-pt/think/topics/prompt-engineering)
4. **Google Cloud - What is Prompt Engineering:** Guia sobre arquitetura Transformer, contextualização e boas práticas para modelos Gemini/PaLM. [Acessar Link](https://cloud.google.com/discover/what-is-prompt-engineering?hl=pt-BR)
5. **Learn Prompting - Introduction:** Documentação interativa e aberta cobrindo fundamentos e técnicas avançadas de interação. [Acessar Link](https://learnprompting.org/docs/introduction)

---

## 3. Engenharia de Prompts e "Cicatrizes" (Troubleshooting) 🛠️

Nesta seção, documentamos os testes realizados no NotebookLM para analisar como variações no estilo de instrução alteram a qualidade da resposta gerada.

### Teste 1: Prompt Vago vs. Prompt Estruturado (Persona + Delimitadores)
* **Prompt Vago:**  
  > *"Como evitar erros no prompt?"*
  * **Resultado:** Resposta genérica, superficial e abrangente demais, sem focar nas boas práticas específicas das fontes do caderno.
* **Prompt Estruturado (Refinado):**  
  > *"Com base nas fontes do caderno, atue como um especialista em IA e explique como resolver os principais problemas ao criar prompts (como alucinações e respostas vagas). Apresente a resposta em formato de tabela comparativa contendo: Problema | Causa | Solução Prática."*
  * **Resultado:** Resposta organizada, objetiva e diretamente vinculada aos conceitos extraídos dos materiais carregados (uso de delimitadores, restrições de escopo e clareza).

### Teste 2: Aplicação da Cadeia de Pensamento (Chain-of-Thought - CoT)
* **Prompt Utilizado:**  
  > *"Explique o processo de troubleshooting ao lidar com alucinações de LLMs. Vamos pensar passo a passo para identificar a causa e aplicar a solução no prompt."*
  * **Aprendizado/Cicatriz:** Estimular a IA a "pensar passo a passo" forçou o NotebookLM a dividir a resposta em etapas lógicas (Diagnóstico de Ambiguidade -> Adição de Delimitadores -> Restrição de Escopo), evitando conclusões apressadas ou simplistas.

### Dificuldades Encontradas e Soluções
* **Respostas Superficiais:** Prompts curtos resultavam em sínteses genéricas. **Solução:** Atribuir uma **Persona** e especificar o **Formato de Saída** desejado (ex: tabelas ou tópicos).
* **Alucinação ou Extrapolação:** Tendência de prever respostas fora do contexto das fontes. **Solução:** Adicionar cláusulas de contenção no comando, como *"Com base estritamente nas fontes inseridas neste caderno..."*.

---

## 4. Miniguia de Estudo (Entrega Final) 📖

### 4.1 Resumo Estruturado do Assunto
* **O que é:** A arte e a ciência de criar comandos otimizados para orientar modelos de IA a gerarem respostas precisas e contextualizadas.
* **Paradigma de Funcionamento:** *Pré-treinar, Prompt e Prever*.
* **Mecanismos Internos:**
  1. **Tokenização:** Decomposição do texto do prompt em unidades menores (tokens).
  2. **Representação Vetorial (Embeddings):** Conversão dos tokens em vetores numéricos de significado.
  3. **Mecanismo de Atenção:** Identificação da relação contextual entre os diferentes tokens.
  4. **Previsão:** Cálculo probabilístico do próximo token mais provável para compor a resposta.

### 4.2 Glossário de Conceitos Key
| Termo | Definição |
| :--- | :--- |
| **LLM** | *Large Language Model*: Modelo de linguagem treinado em vastos volumes de dados de texto. |
| **Token** | A menor unidade de texto processada pelo modelo (pode ser uma palavra ou fragmento de palavra). |
| **Zero-Shot** | Fornecer uma instrução direta à IA sem nenhum exemplo prévio. |
| **Few-Shot** | Fornecer um ou mais exemplos de entrada/saída no contexto do prompt. |
| **Chain-of-Thought (CoT)** | Técnica que orienta o modelo a explicitar suas etapas intermediárias de raciocínio. |
| **Alucinação** | Fenômeno no qual a IA gera informações incorretas ou inventadas com aparência de certeza. |

### 4.3 Prompts Reutilizáveis para Revisão

#### Template 1: Síntese de Conceitos Complexos
    [PAPEL]: Atue como um professor especializado em Inteligência Artificial.
    [TAREFA]: Explique o conceito de [INSERIR TÓPICO] utilizando as fontes do caderno.
    [FORMATO]: 
    1. Uma definição direta de até 2 frases.
    2. Uma analogia do mundo real para facilitar a compreensão.
    3. 3 pontos de atenção principais em bullet points.

#### Template 2: Resolução de Problemas Passo a Passo (CoT)
    [CONTEXTO]: Encontrei a seguinte limitação ao usar a IA: [DESCREVER PROBLEMA].
    [INSTRUÇÃO]: Vamos resolver isso passo a passo:
    1. Identifique a provável causa no prompt original.
    2. Proponha 2 abordagens de correção baseadas em boas práticas.
    3. Reescreva o prompt corrigido com delimitadores claros.

---

## 5. Considerações Finais 🎯

O uso do Google NotebookLM demonstrou o valor da aprendizagem ativa: interagir com as fontes por meio de prompts refinados permite fixar conceitos técnicos com muito mais profundidade do que a leitura passiva. A documentação das "cicatrizes" e o teste de variações comprovam que a clareza e a estrutura do contexto são os pilares fundamentais da engenharia de prompts.
