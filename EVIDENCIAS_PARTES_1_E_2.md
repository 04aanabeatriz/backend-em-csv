# Evidências — Partes 1 e 2

## Identificação

Nome do aluno:
Turma:
Data:

---

## 1. Link do meu repositório GitHub

Cole abaixo o link do seu repositório:

https://github.com/04aanabeatriz/backend-em-csv

---

# Parte 1 — Clonagem, configuração e publicação

## 2. Comprovação do remote configurado

Execute no terminal:

git remote -v

Cole abaixo o resultado:

origin  https://github.com/04aanabeatriz/backend-em-csv.git (fetch)
origin  https://github.com/04aanabeatriz/backend-em-csv.git (push)

---

## 3. Comprovação dos commits

Execute no terminal:

git log --oneline

Cole abaixo o resultado:

cole aqui o resultado

---

## 4. Comprovação do status do projeto

Execute no terminal:

git status

Cole abaixo o resultado:

On branch main
Your branch is up to date with 'origin/main'.

nothing to commit, working tree clean

---

## 5. Comprovação da execução do projeto

Execute no terminal:

npm run dev

Cole abaixo a mensagem exibida no terminal:

Servidor rodando em http://localhost:3000

---

## 6. Teste da rota de todas as leituras

Acesse no navegador:

http://localhost:3000/api/leituras

Cole abaixo parte do resultado exibido:

[
  {
    "id": 1,
    "station_id": "EM-ARACATUBA-01"
  }
]

---

# Parte 2 — Alteração da rota raiz e pesquisa por data

## 7. Comprovação da rota raiz alterada

Acesse no navegador:

http://localhost:3000/

Cole abaixo o resultado exibido:

{
  "mensagem": "API Estação Meteorológica"
}

---

## 8. Teste da rota de pesquisa por data

Acesse no navegador:

http://localhost:3000/api/leituras/data/2026-04-01

Cole abaixo parte do resultado exibido:

{
  "dataPesquisada": "2026-04-01"
}

---

## 9. Teste de data inválida

Acesse no navegador:

http://localhost:3000/api/leituras/data/01-04-2026

Cole abaixo o resultado exibido:

{
  "mensagem": "Formato de data inválido. Use o formato YYYY-MM-DD."
}

---

## 10. Código alterado na rota raiz

Cole abaixo o trecho da rota raiz alterada no arquivo src/server.js:

app.get('/', (req, res) => {
  return res.json({
    mensagem: 'API Estação Meteorológica',
  });
});

---

## 11. Observação final

Consegui clonar, configurar, executar, testar, alterar a rota raiz, testar a pesquisa por data e publicar o projeto no meu GitHub.