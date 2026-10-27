# Applied Prompt Engineering Lab: Análise de Dados do IBGE para Data Storytelling em Redes Sociais

> **Aviso de Uso de Inteligência Artificial:** Este projeto, sua documentação técnica e os pipelines de prompts foram desenvolvidos com assistência de Modelos de Linguagem de Larga Escala (LLMs), atuando como copiloto técnico para pesquisa metodológica, estruturação sintática e validação lógica.

---

## 📋 Contexto Geral

Este estudo de caso documenta a resolução técnica de uma demanda real apresentada em ambiente de pós-graduação: transformar microdados brutos do **Censo Demográfico do IBGE (2022)** em uma narrativa de alto impacto visual e informativo (*data storytelling*) para o **Instagram**, com foco na disparidade de renda média em observar a renda dos bairros dos municípios da **Região Metropolitana de Piracicaba (RMP)** — com ênfase em Anhembi, Piracicaba, Rio Claro e Santa Gertrudes.

Em vez de abordar a IA generativa como um gerador de texto arbitrário, este repositório demonstra como a aplicação rigorosa de **Engenharia de Prompts** garante determinismo, precisão factual e conformidade de tom de voz corporativo.

---

## 🎯 O Desafio

* **Entrada:** Dados censitários de 2022 sobre distribuição de renda domiciliar per capita e setorização censitária/bairros dos municípios:
  * Piracicaba (polo industrial e de serviços)
  * Rio Claro (centro secundário da RMP)
  * Santa Gertrudes (polo cerâmico, menor extensão territorial)
  * Anhembi (característica predominantemente rural e turística)
* **Objetivo:** Criar um carrossel educativo e analítico para o Instagram.
* **Restrições:** Evitar alucinações numéricas, sintetizar disparidades complexas para linguagem leiga e aderir aos limites de caracteres e hierarquia visual das redes sociais.

---

## 🛠️ Técnicas de Engenharia de Prompts Utilizadas

Para evitar respostas genéricas e garantir a integridade dos dados, o problema foi decomposto utilizando um pipeline de 4 técnicas formais:

```mermaid
graph LR
    A[Base IBGE 2022] --> B[1. Decomposição de Tarefas]
    B --> C[2. Context Grounding + CoT]
    C --> D[3. Few-Shot Storytelling]
    D --> E[4. Meta-Review / Self-Refine]
    E --> F[Artefato Final: Post Instagram]
