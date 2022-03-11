# fluxos_ratio
# paf


```mermaid
flowchart TD








  #PAF
  subgraph nmp
    #PAF#NMP
    #PAF#NMP#GABs
  end
  subgraph nmc
    #PAF#NMC
    #PAF#NMC#GABs
  end
  subgraph nif
    #PAF#NIF
    #PAF#NIF#GABs
    #PAF#NIF#DESJUD
  end



CDIST --> #PAF
#PAF --> CDIST

#PAF --> #PAF#NMP
#PAF --> #PAF#NMC
#PAF --> #PAF#NIF

#PAF#NMP --> #PAF
#PAF#NMC --> #PAF
#PAF#NIF --> #PAF


#PAF#NMP --> #PAF#NMP#GABs
#PAF#NMP#GABs --> #PAF#NMP#ARQ
#PAF#NMP#GABs --> #PAF#NIF
#PAF#NMP#GABs --> #PAF#NMP
#PAF#NMP#GABs --> #PAF#NMC
#PAF#NMP#ARQ --> #PAF#NMP


#PAF#NMC --> #PAF#NMC#GABs
#PAF#NMC#GABs --> #PAF#NMP
#PAF#NMC#GABs --> #PAF#NMC
#PAF#NMC#GABs --> #PAF#NIF
#PAF#NMC#GABs --> #PAF#NMC#ARQ
#PAF#NMC#ARQ --> #PAF#NMC



#PAF#NIF --> #PAF#NIF#GABs
#PAF#NIF#GABs --> #PAF#NIF#ARQ
#PAF#NIF#GABs --> #PAF#NMP
#PAF#NIF#GABs --> #PAF#NMC
#PAF#NIF#GABs --> #PAF#NIF
#PAF#NIF --> #PAF#NIF#DESJUD
#PAF#NIF#DESJUD --> #PAF#NMC
#PAF#NIF#DESJUD --> #PAF#NMP
#PAF#NIF#ARQ --> #PAF#NIF







