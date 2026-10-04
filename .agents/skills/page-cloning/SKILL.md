---
name: page-cloning
description: Skill para extrair a estrutura, layout e hierarquia visual de uma página da web existente e reconstruí-la adaptada para um novo produto, mantendo a qualidade do design original.
---

# Page Cloning & Modeling (Clonagem e Adaptação de Páginas)

Quando o usuário pedir para clonar, modelar ou adaptar uma página baseada em uma referência externa (URL ou HTML fornecido), siga rigorosamente o processo abaixo para garantir que a estrutura original seja preservada, mas o conteúdo e a marca sejam adaptados para o produto do usuário.

## 1. Análise da Referência (Scraping Visual e Estrutural)
- **Leitura:** Use a ferramenta `read_url_content` ou o `browser_subagent` para extrair o conteúdo e a estrutura da página de referência. Se o usuário fornecer imagens, use a capacidade multimodal para entender o layout.
- **Mapeamento de Layout:** Identifique as seções principais (Header, Hero, Features, Testimonials, Pricing, Footer). Como o conteúdo está distribuído? (ex: Grid de 3 colunas, Flex-row reverso, etc).
- **Hierarquia Visual:** Observe os tamanhos de fonte (H1, H2, body), peso das fontes e contrastes que guiam o olho do usuário.

## 2. Abstração de Design Tokens
- Em vez de copiar cores e fontes exatas, identifique os *papéis* das cores (Cor Primária, Cor de Fundo, Cor de Texto, Cor de Acento/Destaque).
- Quando for adaptar para o produto do usuário, aplique a paleta de cores e tipografia **do projeto atual** (ou pergunte ao usuário quais devem ser usadas), substituindo os tokens originais pelos novos de forma consistente.

## 3. Substituição de Conteúdo e Contexto
- Entenda o produto do usuário.
- Substitua o texto original (copywriting) por textos que façam sentido para o produto do usuário, mantendo o *tamanho aproximado* dos parágrafos e títulos para não quebrar o layout.
- Se a página original tem uma imagem de um "software de RH", e o produto do usuário é um "app de delivery", sugira ou insira placeholders/imagens adequadas ao novo contexto.

## 4. Reconstrução do Código
- Recrie a estrutura usando as tecnologias do projeto (ex: HTML/CSS Vanilla, React, Tailwind, etc.).
- **NÃO** copie o código-fonte sujo (minificado, com classes aleatórias geradas por frameworks da página original). Em vez disso, **escreva código limpo do zero** que alcance exatamente o mesmo resultado visual e estrutural.
- Garanta que a página seja responsiva, mesmo que você não tenha visto a versão mobile da referência. Aplique boas práticas de UI/UX (use as diretrizes da skill `frontend-design` se aplicável).

## 5. Critérios de Sucesso
- O layout final deve causar a mesma "sensação" de organização e qualidade da referência.
- O código deve ser limpo e mantenível.
- Nenhum texto ou imagem da empresa original deve "sobrar" no resultado final; tudo deve ser adaptado.
