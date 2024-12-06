# Gerador de POP's com Gemini, Guardrails e LaTeX

Este repositório contém uma solução automatizada para a criação de Procedimentos Operacionais Padrão (POPs) utilizando as ferramentas Google Gemini, Guardrails e LaTeX. O código foi desenvolvido para facilitar a criação de POPs de forma padronizada, eficiente e validada, integrando IA generativa, validação de formato e estruturação técnica de documentos.

### Funcionalidades

1. **Interação com o Google Gemini:** O código utiliza a API do Gemini para gerar conteúdos técnicos com base em personas definidas. A interação é realizada por meio de um prompt detalhado, que inclui perfis de especialistas e usuários, permitindo respostas altamente específicas e direcionadas.

2. **Extração de conteúdo TeX:** Através de expressões regulares, o código é capaz de extrair e validar conteúdo LaTeX, garantindo que o POP gerado esteja corretamente estruturado.

3. **Validação com Guardrails:** A integração com o Guardrails e um validador customizado (`ValidTex`) assegura que o conteúdo gerado esteja em conformidade com padrões técnicos, antes de ser impresso ou utilizado.

4. **Execução de Loops Automáticos:** O código pode executar processos automatizados em sequência, validando e aprimorando POPs com base no feedback contínuo entre usuários e especialistas, garantindo a melhoria constante dos documentos.

### Estrutura do Código

- **Interação com o Gemini:** Configura a API do Gemini e interage com o modelo generativo para criar respostas com base em uma descrição de persona.
- **Extração de TeX:** A função `extract_tex_content` captura conteúdo entre os delimitadores LaTeX e o estrutura adequadamente.
- **Validação do TeX:** Antes de finalizar, o código valida o conteúdo extraído com o Guardrails para garantir que esteja conforme os padrões técnicos.

### Como Usar

1. **Configuração Inicial:** 
   - Certifique-se de configurar a chave da API do Google Gemini no arquivo `.env` com a variável `GEMINI_API_KEY`.
   
2. **Executando o Código:**
   - Ao executar o código, insira a pergunta ou descrição do processo que deseja transformar em um POP.
   - O código irá gerar, extrair e validar o código LaTeX correspondente ao POP, validando-o conforme as diretrizes estabelecidas.

3. **Loop de Feedback:**
   - O código está configurado para rodar um loop entre o `usuário` (novato na área) e o `especialista` (engenheiro de produção) para aprimorar o POP com base em sugestões contínuas.

### Requisitos

- **Python 3.x**
- **Bibliotecas:** 
  - `dotenv`
  - `google-generativeai`
  - `guardrails`
  - `re`
  - `Validador_tex`

### Contribuições

Este projeto é de código aberto e aceita contribuições. Sinta-se à vontade para sugerir melhorias, relatar bugs ou adicionar novas funcionalidades.
