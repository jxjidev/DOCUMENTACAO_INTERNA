# Migrar uma demanda

Caso seja necessário migrar uma demanda para produção ou qualquer outro status deverá buscar a demanda na tabela AppDemandas colocando o Where a coluna DemandaSapId e alterar o campo Status conforme lista abaixo:

* Backlog = 0
* Desenvolvimento = 1
* Homologação = 2
* Produção = 3
* Concluído = 4
