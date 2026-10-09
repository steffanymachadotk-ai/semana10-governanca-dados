# Resumo da Entrega · Semana 10 · Governança de Dados

## Arquivos verificados

- [x] `dados/clientes_raw.csv`
- [x] `dados/pedidos_raw.csv`
- [x] `reports/diagnostico_qualidade.csv`
- [x] `reports/expectativas_resultado.csv`
- [x] `dados/clientes_silver_mascarado.csv`
- [x] `governance/catalog.json`
- [x] `governance/lineage_log.json`

## Principais achados de qualidade

- `clientes` · Completude: cidade não pode ser nulo → 25 falhas (20.83%).
- `clientes` · Unicidade: CPF deve ser único → 1 falhas (0.83%).
- `clientes` · Acurácia: email deve conter @ → 3 falhas (2.5%).
- `clientes` · Temporalidade: data_nascimento não pode ser futura → 2 falhas (1.67%).
- `clientes` · Conformidade: status_cliente em {ativo,inativo,bloqueado} → 2 falhas (1.67%).
- `pedidos` · Acurácia: total deve ser positivo → 3 falhas (0.42%).
- `pedidos` · Conformidade: status em {criado,pago,entregue,cancelado} → 2 falhas (0.28%).

## Evidências que devem aparecer no caderno/PDF

- Print do terminal após `00_testar_ambiente.py`.
- Print do relatório `reports/diagnostico_qualidade.html`.
- Print da validação de expectativas (`03_expectativas_gx.py`).
- Print do antes/depois do mascaramento.
- Print do `catalog.json` e/ou `lineage_log.json` no VS Code.
- Respostas escritas explicando risco, técnica aplicada e decisão de governança.