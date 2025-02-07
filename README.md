# Testes Automatizados com Newman e Postman

Este projeto contém testes automatizados para APIs utilizando o **Newman**, executor de linha de comando do **Postman**. Além disso, é possível importar e executar a coleção manualmente no Postman.

## Pré-requisitos

Antes de executar os testes, certifique-se de ter instalado:

- **[Node.js](https://nodejs.org/)** (LTS recomendado)
- **[Postman](https://www.postman.com/)** (opcional, para execução manual)
- **Newman** (instalação explicada abaixo)

---

##  Instalação

1. **Clone este repositório**  
   ```sh
   git clone 
   ```

2. **Instale o Newman**  
   ```sh
   npm install -g newman
   ```

3. **Instale dependências do projeto**  
   ```sh
   npm install
   ```

---

##  Executando os Testes com o Newman

Para executar os testes da coleção **test_api_collection.json** com o ambiente **test_env.json**, utilize o comando:

```sh
newman run test_api_collection.json -e test_env.json
```

### Gerando Relatórios em HTML

Para gerar um relatório no formato HTML, execute:

```sh
newman run test_api_collection.json -e test_env.json -r html
```

O relatório será salvo na pasta **newman/** do projeto.

---

##  Importando Manualmente no Postman

Executar os testes manualmente no Postman:

1. **Abra o Postman**.
2. **Vá até "File" > "Import"**.
3. **Selecione o arquivo** `test_api_collection.json` e clique em **"Import"**.
4. **(Opcional) Importe o ambiente** `test_api_collection.json` na aba **Environments**.
5. **Execute os testes** clicando no botão **"Run Collection"**.

---