# Evidências - INSERT, UPDATE e DELETE no banco db_em

## Identificação

Nome: Ana Beatriz  
Turma: 3A  
Data: 21/05/2026

---

# 1. SELECT final - Leituras do dia 2026-04-04

```sql
SELECT *
FROM leituras
WHERE timestamp >= '2026-04-04'
AND timestamp < '2026-04-05'
ORDER BY timestamp ASC;
```

```text
Cole aqui o resultado que apareceu no DBeaver.
```

---

# 2. SELECT final - Conferência do UPDATE

```sql
SELECT *
FROM leituras
WHERE station_id = 'EM-ARACATUBA-01'
AND timestamp = '2026-04-04 09:00:00';
```

```text
Cole aqui o resultado mostrando:
temperature_c = 25.2
humidity_pct = 72.0
```

---

# 3. SELECT final - Conferência do DELETE

```sql
SELECT *
FROM leituras
WHERE station_id = 'EM-ARACATUBA-01'
AND timestamp = '2026-04-04 11:00:00';
```

```text
Sem registros encontrados.
```

---

# 4. SELECT final - Todas as leituras ordenadas

```sql
SELECT *
FROM leituras
ORDER BY id ASC;
```

```text
Cole aqui o resultado completo.
```

---

# 5. Teste pela API

```text
http://localhost:3000/api/leituras/data/2026-04-04
```

```json
{
  "dataPesquisada": "2026-04-04",
  "total": 3,
  "leituras": [
    {
      "station_id": "EM-ARACATUBA-01",
      "temperature_c": 23.4,
      "humidity_pct": 76.2
    },
    {
      "station_id": "EM-ARACATUBA-01",
      "temperature_c": 25.2,
      "humidity_pct": 72.0
    },
    {
      "station_id": "EM-ARACATUBA-01",
      "temperature_c": 25.9,
      "humidity_pct": 70.5
    }
  ]
}
```

---

# 6. Conclusão

Resposta:

```text
INSERT adiciona novos registros na tabela.
UPDATE altera registros existentes.
DELETE remove registros da tabela.
O WHERE é importante para alterar ou excluir apenas os registros desejados.
```