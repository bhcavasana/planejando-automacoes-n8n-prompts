# Prompt Final — Planejando Automações com N8N Usando Apenas Bons Prompts

## Passo 1: Defina a automação desejada

```text
Quero criar uma automação no N8N para triagem inteligente, classificação com IA e agendamento automático de leads e solicitações comerciais recebidas via formulário web.

Público ou responsável:
Equipe comercial (SDRs e Executivos de Contas) e time de Atendimento ao Cliente.

Resultado esperado:
Classificar automaticamente a urgência e o perfil do lead usando o Google Gemini, salvar os dados validados em uma planilha no Google Sheets, agendar follow-up no Google Calendar para leads quentes, enviar e-mail de confirmação pelo Gmail e notificar o time de vendas via Telegram.
```

---

## Passo 2: Adicione contexto e regras

```text
Ferramentas envolvidas:
Webhook (Formulário Web), Google Gemini (AI Agent), Google Sheets, Google Calendar, Gmail e Telegram.

Fluxo desejado:
1. Receber uma nova resposta do formulário via Webhook.
2. Validar o formato do e-mail e o conteúdo da mensagem.
3. Classificar a intenção, prioridade e gerar um resumo da solicitação com o Google Gemini.
4. Registrar os dados do lead e a classificação da IA na planilha do Google Sheets.
5. Agendar follow-up no Google Calendar caso seja uma oportunidade comercial de alta prioridade.
6. Enviar um e-mail de confirmação ao cliente via Gmail e notificar a equipe no Telegram.

Regras importantes:
- Ignorar registros sem e-mail válido ou com mensagem vazia/menor que 10 caracteres.
- Validar a resposta da IA em formato JSON estruturado (Structured Output Parser) antes de salvar na planilha.
- Em caso de falha de comunicação com alguma API externa, executar nova tentativa (Retry) e registrar o erro sem interromper o fluxo principal.
```

---

## Passo 3: Prompt Final Consolidado

```text
Atue como um especialista em N8N.

Crie uma automação para triagem inteligente, classificação com IA e encaminhamento automático de leads recebidos por formulário.

Público:
Equipe comercial (SDRs e Executivos de Contas) e time de Atendimento ao Cliente.

Ferramentas envolvidas:
Webhook, Google Gemini (AI Agent), Google Sheets, Google Calendar, Gmail e Telegram.

Fluxo:
Receber uma resposta via Webhook, validar o e-mail, classificar a intenção e prioridade do lead usando o Google Gemini, salvar os dados enriquecidos na planilha do Google Sheets, criar um evento de follow-up no Google Calendar para leads de alta prioridade, enviar um e-mail de confirmação via Gmail e notificar o time comercial no Telegram.

Regras:
Ignorar registros sem e-mail válido ou mensagens com menos de 10 caracteres, garantir saída JSON estruturada da IA (Structured Output Parser) e tratar erros de API com Retry e Error Trigger.

Explique quais nós do N8N devem ser utilizados e a lógica de funcionamento do workflow.
```
