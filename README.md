# 🎙️ Gerador de Podcast com IA (Gemini) no Google Colab

Crie podcasts envolventes onde duas Inteligências Artificiais (Google Gemini) debatem um tema escolhido por você! Este projeto para Google Colab transforma sua ideia em um arquivo MP3 pronto para ouvir, orquestrando todo o diálogo e a conversão para áudio.

[![Abra no Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/186ilUKQh1iSb3ITSadiuTrspndrYTgnd?usp=sharing)

![image](https://github.com/user-attachments/assets/140395f3-a0fa-4a74-80d7-e647a4975bd9)

<!-- Opcional: Adicione um GIF ou imagem de exemplo do output ou do player no Colab -->
<!-- ![Exemplo de Podcast Gerado]([LINK_PARA_IMAGEM_EXEMPLO_AQUI]) -->

## ✨ Funcionalidades

*   **Tema Personalizado:** O usuário define o tópico da discussão.
*   **Agentes de IA Configuráveis:** Duas IAs (Eu otimista, e Eu mesmo analítico) com personalidades distintas debatem o tema.
    *   Utiliza o SDK do **Google Gemini** (modelo `gemini-2.0-flash` por padrão).
    *   Prompts de sistema detalhados para guiar o comportamento dos agentes.
*   **Geração de Diálogo Dinâmico:** As IAs respondem uma à outra, criando uma conversa fluida.
*   **Conversão para Áudio (TTS):**
    *   Utiliza `gTTS` para converter o texto em fala (português do Brasil).
    *   Inclui introdução e conclusão automáticas no podcast.
*   **Saída em MP3:** O resultado final é um arquivo `.mp3` contendo o podcast completo.
*   **Execução no Google Colab:** Fácil de rodar, sem necessidade de instalações complexas localmente.
*   **Player de Áudio Embutido:** Ouça o podcast diretamente na saída do Colab.

## 🚀 Como Usar

1.  **Abra no Google Colab:**
    *   Clique no botão [![Abra no Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/186ilUKQh1iSb3ITSadiuTrspndrYTgnd?usp=sharing) acima.
    *   Ou acesse diretamente: `(https://colab.research.google.com/drive/186ilUKQh1iSb3ITSadiuTrspndrYTgnd?usp=sharing)`

2.  **Configure sua API Key do Gemini:**
    *   Obtenha sua API Key no [Google AI Studio](https://aistudio.google.com/app/apikey).
    *   No Colab, vá no painel esquerdo, clique no ícone de chave (🔑 **Secrets**).
    *   Adicione um novo segredo com o nome `GOOGLE_API_KEY` e cole sua chave no campo "Value".
    *   Certifique-se de que "Notebook access" está habilitado para este segredo.

3.  **Instale as Dependências:**
    *   Execute a primeira célula de código do notebook, que contém:
        ```python
        !pip install -q google-generativeai gTTS pydub
        ```

4.  **Execute o Script Principal:**
    *   Execute a(s) célula(s) seguintes que contêm o código do gerador de podcast.
    *   Você será solicitado a **digitar o tema** para a discussão das IAs.

5.  **Aguarde e Ouça/Baixe:**
    *   O script irá gerar o diálogo e o arquivo de áudio.
    *   Um player de áudio aparecerá na saída da célula para você ouvir o podcast.
    *   O arquivo MP3 (ex: `meu_podcast_com_gemini.mp3`) também estará disponível no painel de arquivos à esquerda para download.

## 🛠️ Configurações (Opcionais no Código)

Dentro do script, você pode ajustar:

*   `NUM_TURNS`: Número de turnos de fala para cada agente (controla a duração).
*   `MODEL_TO_USE`: Modelo do Gemini a ser utilizado (ex: `"gemini-1.0-pro-latest"` para um modelo mais robusto, pode ter custos diferentes).
*   **Prompts dos Agentes:** Modifique os `agentX_system_info` para alterar as personalidades ou instruções das IAs.
*   **Textos de Introdução/Conclusão:** Personalize as mensagens de abertura e fechamento do podcast.

## 🔧 Dependências Principais

*   `google-generativeai`: SDK oficial do Google para a API Gemini.
*   `gTTS`: Google Text-to-Speech, para converter texto em áudio.
*   `pydub`: Para manipulação de áudio e exportação para MP3.
*   `IPython`: Para exibir o player de áudio no Colab.

## 🔮 Próximos Passos e Ideias para Melhorias

*   [ ] Permitir a seleção de diferentes vozes/idiomas para os agentes (requereria uma biblioteca de TTS mais avançada, como a API Google Cloud Text-to-Speech).
*   [ ] Adicionar música de fundo ou efeitos sonoros.
*   [ ] Interface de usuário mais elaborada (ex: com Gradio ou Streamlit, se sair do Colab).
*   [ ] Opção para o usuário definir os prompts de sistema dos agentes.
*   [ ] Melhor controle sobre a duração final do podcast.

## 🤝 Contribuições

Contribuições são bem-vindas! Sinta-se à vontade para abrir *issues* ou enviar *pull requests* com melhorias, correções de bugs ou novas funcionalidades.

## 📄 Licença

Este projeto é distribuído sob a licença MIT. Veja o arquivo `LICENSE` para mais detalhes. (Você precisará criar um arquivo LICENSE se quiser especificar uma).

---

*Feito com ❤️ e 🧠 por Marcos Eduardo Elorza*
*Inspirado na exploração de IAs conversacionais e geração de conteúdo.*
