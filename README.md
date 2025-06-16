# 🚀 Laboratório Prático: Análise de Fala e Linguagem Natural com Azure AI Services

Bem-vindo ao repositório do projeto desenvolvido como parte do desafio "Construa um Perfil de Destaque na DIO", focado na exploração e aplicação das ferramentas **Azure Speech Studio** e **Azure Language Studio**. Este projeto visa aprofundar o entendimento e as habilidades práticas no uso de Inteligência Artificial para análise de voz e texto, documentando o processo de forma clara e estruturada.

## 🎯 Objetivos do Desafio

O principal objetivo deste laboratório foi desenvolver proficiência nas ferramentas de IA da Microsoft Azure, especificamente no que tange ao processamento de fala (Speech-to-Text, Text-to-Speech) e análise de linguagem natural (extração de entidades, análise de sentimento, etc.). Ao final, o projeto busca consolidar os seguintes aprendizados:

* **Aplicar conceitos teóricos** em um ambiente prático e real, utilizando serviços de nuvem.
* **Documentar processos técnicos** de forma clara, concisa e estruturada, facilitando a compreensão e replicação.
* **Utilizar o GitHub** como uma ferramenta eficaz para versionamento de código, colaboração e, principalmente, para o compartilhamento de documentação técnica.

## 🛠️ Ferramentas e Tecnologias Utilizadas

* **Microsoft Azure Cloud:** Plataforma de serviços de nuvem.
* **Azure AI Services:** Conjunto de APIs e serviços de IA, incluindo:
    * **Azure Speech Studio:** Para funcionalidades de fala (conversão de fala em texto, síntese de fala).
    * **Azure Language Studio:** Para funcionalidades de linguagem natural (análise de sentimento, extração de entidades, etc.).
* **GitHub:** Para controle de versão e hospedagem do repositório.
* **Markdown:** Linguagem de marcação para formatação de texto (utilizada neste `README`).

## 📁 Estrutura do Repositório

Este repositório está organizado da seguinte forma para facilitar a navegação e compreensão do conteúdo:
├── .github/          # (Opcional) Configurações de workflows ou templates
├── images/           # Capturas de tela e recursos visuais do projeto
│   ├── speech_studio_overview.png
│   ├── speech_to_text_example.png
│   ├── language_studio_sentiment.png
│   └── ...
├── README.md         # Este arquivo: documentação completa do projeto
└── src/              # (Opcional) Pequenos trechos de código ou exemplos de dados
├── audio_samples/
└── text_samples/


## 🚀 Mão na Massa: A Experiência Prática

Nesta seção, detalhamos os passos e as descobertas feitas ao interagir com o Azure Speech Studio e o Azure Language Studio.

### 🎤 1. Explorando o Azure Speech Studio

O Azure Speech Studio oferece um conjunto robusto de ferramentas para transformar fala em texto e texto em fala, além de recursos avançados para personalização de modelos.

#### **1.1. Configuração Inicial**

Para iniciar, foi necessário criar um recurso de "Serviços de Fala" (Speech Service) no portal do Azure.
* **Passos:** Navegar até "Criar um recurso" > Pesquisar por "Speech" > Selecionar "Speech" > Configurar região, nome e plano de preços (utilizado o plano gratuito para testes).
* **Chaves e Endpoint:** Após a criação, as chaves de assinatura e o endpoint da região foram obtidos para autenticação nos serviços.

#### **1.2. Conversão de Fala em Texto (Speech-to-Text)**

Exploramos a funcionalidade de transcrever áudios para texto.

* **Funcionalidade:** No Speech Studio, acessamos a seção "Conversão de fala em texto" e "Reconhecimento em tempo real".
* **Exemplo Prático:**
    * Foi carregado um pequeno arquivo de áudio (ou utilizado o microfone) com a frase "Olá, este é um teste de reconhecimento de fala da DIO."
    * **Resultado:** O serviço transcreveu com alta precisão a frase. Observamos a capacidade de identificar pausas e pontuações automaticamente.
    * **Insights:** A precisão do reconhecimento é impressionante, mesmo com nuances na fala. A interface permite visualizar a confiança de cada palavra reconhecida.
* **Customização (Opcional):** Exploramos brevemente as opções de modelos de reconhecimento de fala personalizados, que permitem treinar o serviço para vocabulários específicos (ex: termos técnicos de uma indústria).
    * **[!] Ver imagem:** `images/speech_to_text_example.png` - Exemplo de transcrição de fala em texto.

#### **1.3. Síntese de Fala (Text-to-Speech)**

Investigamos a capacidade do Speech Studio de converter texto em fala, utilizando diferentes vozes e estilos.

* **Funcionalidade:** Acessamos a seção "Síntese de fala" e "Áudio de fala".
* **Exemplo Prático:**
    * Digitamos frases como "Bem-vindos ao mundo da Inteligência Artificial com a Microsoft Azure!" e "A documentação é a chave para o sucesso de qualquer projeto técnico."
    * **Vozes e Estilos:** Experimentamos diversas vozes neurais (ex: `pt-BR-FranciscaNeural`, `pt-BR-AntonioNeural`), alterando a entonação, velocidade e volume. As vozes neurais são notavelmente realistas.
    * **SSML (Speech Synthesis Markup Language):** Demonstramos o uso de SSML para controlar aspectos avançados da fala, como pausas `<break time="500ms"/>` e ênfase `<emphasis level="moderate">importante</emphasis>`.
    * **Insights:** A variedade e a qualidade das vozes neurais são um grande diferencial, permitindo criar experiências de áudio muito naturais para diversas aplicações (assistentes virtuais, audiolivros, etc.).
    * **[!] Ver imagem:** `images/text_to_speech_options.png` - Exemplo de opções de síntese de fala.

### 📝 2. Dissecando a Linguagem com Azure Language Studio

O Azure Language Studio oferece uma plataforma para explorar e aplicar os serviços de Processamento de Linguagem Natural (PLN) da Microsoft Azure.

#### **2.1. Configuração Inicial**

Similar ao Speech Studio, um recurso de "Serviços Cognitivos" ou especificamente um "Serviço de Linguagem" foi criado no Azure Portal.
* **Passos:** "Criar um recurso" > Pesquisar por "Language Service" > Selecionar "Language Service" > Configurar.

#### **2.2. Análise de Sentimento**

Esta funcionalidade avalia o tom emocional de um texto (positivo, negativo, neutro ou misto).

* **Funcionalidade:** No Language Studio, acessamos "Analisar texto" e selecionamos "Análise de sentimento".
* **Exemplo Prático:**
    * **Texto 1:** "Este desafio da DIO é extremamente enriquecedor e a documentação é fantástica!"
    * **Resultado 1:** Predominantemente positivo, com alta pontuação de confiança.
    * **Texto 2:** "O projeto teve alguns contratempos, mas a equipe conseguiu superá-los com sucesso."
    * **Resultado 2:** Sentimento misto, com detecção de partes negativas e positivas na mesma frase.
    * **Insights:** A capacidade de granularidade na análise de sentimento (por frase e por documento) é muito útil para entender a nuance das opiniões.
    * **[!] Ver imagem:** `images/language_studio_sentiment.png` - Exemplo de análise de sentimento.

#### **2.3. Extração de Entidades (Named Entity Recognition - NER)**

Identifica e categoriza entidades importantes em um texto, como nomes de pessoas, locais, organizações, datas e muito mais.

* **Funcionalidade:** No Language Studio, acessamos "Extração de entidades nomeadas".
* **Exemplo Prático:**
    * **Texto:** "Maria Silva, CEO da Tech Solutions, esteve em São Paulo em 15 de junho de 2025 para uma reunião importante sobre o novo produto X."
    * **Resultados:**
        * `Maria Silva`: Pessoa
        * `Tech Solutions`: Organização
        * `São Paulo`: Local
        * `15 de junho de 2025`: Data
        * `produto X`: Produto
    * **Insights:** Essencial para a mineração de dados e para estruturar informações não estruturadas de textos, muito útil em chatbots, sistemas de busca e automação.

#### **2.4. Detecção de PII (Personally Identifiable Information)**

Identifica e categoriza informações que podem ser usadas para identificar um indivíduo.

* **Funcionalidade:** No Language Studio, acessamos "Identificação de informações de identificação pessoal".
* **Exemplo Prático:**
    * **Texto:** "Por favor, envie o relatório para joao.silva@email.com. Meu telefone é (11) 98765-4321 e meu RG é 12.345.678-9."
    * **Resultados:** O serviço detectou e categorizou o e-mail, número de telefone e RG como PII.
    * **Insights:** Crucial para conformidade com privacidade de dados (LGPD, GDPR) e para mascarar informações sensíveis em logs ou sistemas.

## 🧠 Aprendizados e Conclusões

Este laboratório prático com Azure Speech Studio e Language Studio foi uma experiência enriquecedora que solidificou vários conceitos de Inteligência Artificial. Os principais aprendizados incluem:

* **Facilidade de Uso:** As interfaces do Speech Studio e Language Studio são intuitivas e permitem o rápido prototipagem e teste de funcionalidades de IA.
* **Poder dos Modelos Pré-treinados:** A qualidade dos modelos de IA da Microsoft é impressionante, oferecendo alta precisão para tarefas complexas como reconhecimento de fala e análise de sentimento sem a necessidade de grande volume de dados para treinamento inicial.
* **Versatilidade:** Os serviços podem ser aplicados em uma vasta gama de cenários, desde assistentes de voz e transcrição de reuniões até análise de feedback de clientes e anonimização de dados.
* **Importância da Documentação:** A prática de documentar cada passo e insight é fundamental para consolidar o aprendizado, servir como referência futura e compartilhar conhecimento de forma eficaz. O GitHub provou ser uma plataforma excelente para essa finalidade.
* **Habilidades de Engenharia de Prompt/Interação:** Embora não seja o foco principal, a interação com esses serviços nos ensina a formular "entradas" (áudio, texto) de forma que a IA possa processá-las da melhor maneira.

## 🔗 Recursos Úteis e Referências

* [Explore Speech Studio - Laboratório no Microsoft Learning](https://learn.microsoft.com/en-us/training/modules/explore-speech-studio/)
* [Analyze text with Language Studio - Laboratório no Microsoft Learning](https://learn.microsoft.com/en-us/training/modules/analyze-text-language-studio/)
* [GitHub Quick Start - Repositório com Link para Aulas de Git e GitHub](https://github.com/digitalinnovationone/github-quickstart)
* [GitBook: Formação GitHub Certification - Material textual sobre GitHub](https://www.dio.me/articles/formacao-github-certification)
* [Documentação Oficial do GitHub - Guia completo para uso do GitHub](https://docs.github.com/pt/get-started/onboarding/getting-started-with-github)
* [Guia de Sintaxe Markdown do GitHub](https://docs.github.com/en/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax)

## ✍️ Autor

* **[Jonata Mendes]**
* [Link para seu Perfil na DIO] https://www.dio.me/users/cybermagog

---

Este `README.md` é uma demonstração do meu compromisso com a documentação técnica e o aprendizado contínuo em Inteligência Artificial. Espero que ele seja útil para outros estudantes e profissionais!

---
