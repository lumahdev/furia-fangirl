# Fani, a Fangirl

**Fani, uma Fangirl** é um chatbot criado especialmente para fãs dos times de CS da **FURIA** que querem saber tudo sobre eles. Chega de abrir 300 telas para fazer perguntas sobre seu time favorito ou procurar informações que você não encontra em lugar nenhum, basta perguntar para a **Fani** e o histórico das suas mensagens será salvo.

## Screenshots
![Screenshot](./screenshots/2_screenshot.png)

## Tecnologias
- React
- TypeScript
- Flask
- Vercel
- SQLite
- Docusaurus
- API OpenAI

## Funcionalidades
- Receber mensagens da equipe de suporte ao cliente da FURIA e responder corretamente;
- Interpretar o contexto da mensagem, selecionando corretamente o banco de dados a ser utilizado;
- Respeitar as regras e responder apenas a perguntas relacionadas à FURIA.


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
