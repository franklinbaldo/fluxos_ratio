# fluxos_ratio
# paf


```mermaid
flowchart TD

subgraph FLUXOS_PAF[FLUXOS PAF]
  PAF((PAF)) --> NMP(NMP)
  PAF((PAF)) --> NIF(NIF)
  PAF((PAF)) --> NMC(NMC)
end

subgraph FLUXOS_NMP[FLUXOS NMP]
 
end

subgraph atos_constritivos 
  inicio_prescricao(Início da prescrição) --> verifica_devedor{Tipo devedor?}
  verifica_devedor --> |CPF| devedor_cpf((CPF))
  devedor_cpf --> devedor_ativo
  verifica_devedor --> |CNPJ| devedor_cnpj
  subgraph rotina_prescricao
    verificar_prescricao{Está prescrito?}
    verificar_prescricao --> |Sim| peticiona_prescricao_intercorrente
    verificar_prescricao --> |Não| verifica_devedor
  end
end

subgraph rotina_cnib
  verifica_cnib{Decretado CNIB?}
  verifica_cnib --> |Sim| cnib_decretado
  verifica_cnib --> |Não| tipo_divida{Tipo Divida?}
  tipo_divida --> |Tributária| peticiona_cnib
  tipo_divida --> |Não Tributária| verificar_prescricao
  peticiona_cnib --> verifica_cnib
  peticiona_cnib --> cnib_decretado 
  cnib_decretado --> |Depois de 1 ano| verificar_prescricao
end
