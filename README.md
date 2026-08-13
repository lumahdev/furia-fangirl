# 🙋‍♀️ Fani Chatbot

**Fani, uma Fangirl** é um chatbot criado especialmente para fãs dos times de CS da **FURIA** que querem saber tudo sobre eles. Chega de abrir 300 telas para fazer perguntas sobre seu time favorito ou procurar informações que você não encontra em lugar nenhum, basta perguntar para a **Fani** e o histórico das suas mensagens será salvo.

## Screenshots
![Screenshot](./screenshots/2_screenshot.png)
<img width="1920" height="963" alt="image" src="https://github.com/user-attachments/assets/bac79d60-15f6-46e1-804f-b8fbc010bf05" />


## Tecnologias
- React
- TypeScript
- Flask
- Vercel
- SQLite
- Docusaurus
- API OpenAI

# Funcionalidades principais
- Receber mensagens a respeito do time de CS da FURIA e responder com precisão;
- Interpretação do contexto da mensagem, resultando na escolha correta do banco de dados a ser utilizado;
- Respeitar as regras e seguir o contexto de responder somente perguntas relacionadas a FURIA.

## Exemplos de resposta
A **Fani** reconhece corretamente o seu objetivo e escopo de perguntas que podem ser respondidas.

<img width="1221" height="226" alt="image" src="https://github.com/user-attachments/assets/23e8b2cd-8cd5-48de-b182-1fd69805f270" />

<img width="1215" height="221" alt="image" src="https://github.com/user-attachments/assets/a155ac76-f707-4895-b268-71937cead5af" />


Apesar de não haver uma definição clara de CS-GO no banco de dados, **Fani** entende que a pergunta está dentro do escopo e responde adequadamente a pergunta do usuário.

<img width="1447" height="246" alt="image" src="https://github.com/user-attachments/assets/bf13be92-93ba-40e9-ab2b-c8b5fa1104f7" />


## Variáveis ​​de ambiente
No arquivo ```.env.example```, você pode visualizar as variáveis ​​de ambiente usadas pelo projeto.
- Crie o arquivo ```.env``` no diretório ```frontend``` e atribua o valor da variável ```REACT_APP_API_URL```;
- Crie o arquivo ```.env``` no diretório ```backend``` e atribua o valor da variável ```OPENAI_KEY```.

## Endpoints
Abaixo está uma lista de todos os endpoints disponíveis.

### Enviar mensagem
#### URL
```bash
POST /api/query/
```

#### Request header
```bash
Content-Type: application/json
```

#### Request body
```bash
{
  "input": "qual o squad atual da FURIA?"
}
```

#### Exemplo de resposta
```bash
{
  "response": "O squad atual da FURIA no CS:GO \u00e9 composto por Yuri \"yuurih\" Boian, Kaike 
  \"KSCERATO\" Cerato, Gabriel \"FalleN\" Toledo, Danil \"molodoy\" Golubenko e Mareks \"YEKINDAR\"
  Ga\u013cinskis (este \u00faltimo como stand-in). Sidnei \"sidde\" Macedo atua como t\u00e9cnico da 
  equipe."
}
```
