# Dia 1 – Conversor CSV → SQL Insert (sem BULK INSERT)

Este projeto lê um arquivo CSV e insere os dados diretamente em uma tabela SQL Server via `pyodbc`.

## 🎯 Objetivo

- Ler um arquivo `.csv`
- Gerar comandos `INSERT INTO` para uma tabela SQL Server
- Executar os inserts diretamente via `pyodbc` (sem usar `BULK INSERT`)
- Possibilitar reuso para qualquer CSV e qualquer tabela destino

## 📦 Estrutura de Arquivos

```
csv_to_sql_insert/
├── csv-to-sql-Server-insert.py
├── exemplo.csv
├── .env
├── README.md
```

## ✅ Como usar

1. Instale as dependências:

```bash
pip install pandas pyodbc python-dotenv
```

2. Preencha o arquivo `.env` com suas configurações:

```env
SQL_SERVER=SEU_SERVIDOR
SQL_DATABASE=SUA_BASE
SQL_USERNAME=SEU_USUARIO
SQL_PASSWORD=SUA_SENHA
SQL_TABLE=sua_tabela_destino
CSV_FILE=exemplo.csv
```

3. Rode o script:

```bash
python csv-to-sql-Server-insert.py
```

## 📌 Observações

- Evita o uso de `BULK INSERT`, ideal para ambientes com restrições.
- Trata valores `NULL` e escapa apóstrofos.
- Flexível para qualquer CSV com estrutura compatível com a tabela destino.

- 
## 👨‍💻 Autor

Desenvolvido por [Welson Viana](https://github.com/Welsonvv)

---

## 🛡️ Licença

MIT License
