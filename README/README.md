# <img src="https://img.icons8.com/fluency/48/000000/artificial-intelligence.png" width="38" align="top"/> Azure AI Search — Mineração de Conhecimento com Inteligência Artificial

![Azure](https://img.shields.io/badge/Azure-0078D4?style=flat-square&logo=microsoft-azure&logoColor=white)
![AI Search](https://img.shields.io/badge/AI%20Search-6E32A5?style=flat-square&logo=azuredevops&logoColor=white)
![AI Services](https://img.shields.io/badge/AI%20Services-5DBCD2?style=flat-square&logo=databricks&logoColor=white)
![Storage](https://img.shields.io/badge/Blob%20Storage-2D7D46?style=flat-square&logo=microsoft-azure&logoColor=white)
![Portal](https://img.shields.io/badge/Azure%20Portal-2C2C31?style=flat-square&logo=windows11&logoColor=white)
![Search Explorer](https://img.shields.io/badge/Search%20Explorer-4D8AF0?style=flat-square&logo=search&logoColor=white)
![JSON API](https://img.shields.io/badge/REST%20API-F06449?style=flat-square&logo=json&logoColor=white)
![Power BI](https://img.shields.io/badge/Power%20BI-F6C915?style=flat-square&logo=powerbi&logoColor=white)
![Status](https://img.shields.io/badge/Experimental-FF6F00?style=flat-square&logo=flask&logoColor=white)
![License](https://img.shields.io/badge/MIT-29ABE2?style=flat-square&logo=github&logoColor=white)
![GitHub](https://img.shields.io/badge/GitHub-24292f?style=flat-square&logo=github&logoColor=white)

---

**Contexto e Objetivo**  
Este projeto demonstra, de modo inovador e prático, como transformar avaliações de clientes em ativos estratégicos de conhecimento utilizando recursos avançados da plataforma Azure. O objetivo central é estruturar, enriquecer e organizar grandes volumes de informações com IA, facilitando a busca, análise e geração de insights relevantes para o negócio.

---

## 🛠️ Ferramentas Azure & Funcionalidades

- <img src="https://img.icons8.com/color/48/000000/azure-1.png" width="22"/> **Azure AI Search**  
  Criação de índices inteligentes, pesquisa semântica e filtros avançados.
- <img src="https://img.icons8.com/color/48/000000/artificial-intelligence.png" width="22"/> **Azure AI Services**  
  Enriquecimento automático de dados com análise de sentimento, extração de frases-chave, reconhecimento de entidades e processamento de imagens.
- <img src="https://img.icons8.com/color/48/000000/microsoft-azure-storage.png" width="22"/> **Azure Storage Account (Blob Storage)**  
  Armazenamento seguro de documentos originais, dados enriquecidos e projeções analíticas.
- <img src="https://img.icons8.com/fluency/48/000000/portal.png" width="22"/> **Azure Portal & Search Explorer**  
  Interface intuitiva para provisionamento, configuração e exploração dos recursos.
- <img src="https://img.icons8.com/color/48/000000/json--v1.png" width="22"/> **JSON/REST API**  
  Consulta avançada e integração de resultados.
- <img src="https://img.icons8.com/color/48/000000/power-bi.png" width="22"/> **Power BI**  
  Visualização e análise integrada dos dados enriquecidos.

**Funcionalidades-chave:**  
- Ingestão automatizada e segura de documentos.
- Enriquecimento de conteúdo via IA, trazendo contexto prático e semântico.
- Pesquisas avançadas por múltiplos critérios (localidade, sentimento, entidades, imagens).
- Persistência e análise de dados enriquecidos no Knowledge Store para integração e BI.

---

## 📑 Estrutura da Documentação

```
/
├── README/
│   └── README.md       # Visão geral, contexto, ferramentas, guia de execução e instruções
├── INSIGHTS/
│   └── INSIGHT.md      # Insights práticos e recomendações técnicas
├── PROMPTS.md          # Exemplos, testes e comandos para reprodução
├── LICENSE             # Termos de licença do projeto
├── screenshots/        # Evidências visuais do processo
```

> **A documentação é estruturada, sequencial e orientada à reprodução, facilitando o entendimento, implementação e auditoria do experimento.**

---

## 👨‍💻 Guia de Execução Profissional

### 1️⃣ Provisionamento dos Recursos Azure

- Crie um grupo de recursos dedicado.
- Implemente:
  - **Azure AI Search** (Basic)
  - **Azure AI Services** (Standard S0)
  - **Azure Storage Account** (Standard, LRS, com acesso anônimo para blobs)
- Garanta que todos estejam na mesma região para integração eficiente.

---

### 2️⃣ Upload & Organização dos Dados

- No **Azure Portal** <img src="https://img.icons8.com/fluency/48/000000/portal.png" width="18"/>, crie o container `coffee-reviews` com acesso público.
- Faça upload dos arquivos de avaliações de clientes para o container.

---

### 3️⃣ Indexação e Enriquecimento Automatizado

- No **Azure AI Search** <img src="https://img.icons8.com/color/48/000000/azure-1.png" width="18"/>, inicie o assistente "Import Data".
- Conecte ao container de dados.
- Adicione skills cognitivas <img src="https://img.icons8.com/color/48/000000/artificial-intelligence.png" width="18"/>:
  - OCR (para extração de texto)
  - Extração de localização, frases-chave, sentimento
  - Tags e legendas automáticas para imagens
- Configure o **Knowledge Store** para armazenar projeções enriquecidas no container `knowledge-store`.
- Defina campos do índice como filtráveis e pesquisáveis conforme a necessidade analítica.

---

### 4️⃣ Execução & Monitoramento do Indexador

- Nomeie o indexador como `coffee-indexer` e execute-o.
- Monitore o status no **Azure Portal** até obter "success".

---

### 5️⃣ Exploração, Validação & Consultas

- Use o **Search Explorer** <img src="https://img.icons8.com/color/48/000000/search--v1.png" width="18"/> para realizar queries dinâmicas, por exemplo:
    - Busca ampla (`*`)
    - Filtros por localidade (`locations:'Chicago'`)
    - Filtros por sentimento (`sentiment:'negative'`)
- Navegue no **Knowledge Store** via **Azure Storage** para visualizar projeções e tabelas enriquecidas.
- Realize integrações e visualizações no **Power BI** <img src="https://img.icons8.com/color/48/000000/power-bi.png" width="18"/> para análises avançadas.

---

### 6️⃣ Registro de Evidências & Resultados

- Capture e armazene screenshots de todas as etapas e principais resultados.
- Documente observações e aprendizados em `INSIGHTS/INSIGHT.md`.

---

## 🧠 Insights Estratégicos & Recomendações

- O enriquecimento por IA proporciona visão aprofundada sobre a experiência do cliente, permitindo identificar padrões, tendências e oportunidades de melhoria.
- A persistência de dados no Knowledge Store viabiliza integrações analíticas e relatórios corporativos robustos.
- Recomenda-se sempre garantir consistência regional dos recursos Azure e revisar políticas de acesso para garantir segurança.
- A solução pode ser expandida para automação de atendimento, monitoramento de reputação e priorização de melhorias em produtos e serviços.

---
<p align="center" style="background:#0A2342; padding:20px;">
  <strong style="color:#dfe6e9;">
    Desenvolvido por Huntercode918 
    <img src="https://img.icons8.com/fluency/24/000000/artificial-intelligence.png" width="22" align="top" alt="AI Icon"/>
    | Para mais informações, consulte os arquivos do projeto
  </strong>
</p>
