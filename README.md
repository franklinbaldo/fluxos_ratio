# fluxos_ratio
# paf


```mermaid
flowchart TD




CDIST --> #PAF
#PAF --> CDIST

#PAF#NIF#DESJUD

#PAF --> #PAF#NMP
#PAF --> #PAF#NMC
#PAF --> #PAF#NIF

#PAF#NMP --> #PAF#NMP#GABs
#PAF#NMP --> #PAF
#PAF#NMP#GABs --> #PAF#NIF

#PAF#NMC --> #PAF#NMC#GABs
#PAF#NMC --> #PAF

#PAF#NIF --> #PAF#NIF#GABs
#PAF#NIF --> #PAF
#PAF#NIF#DESJUD --> #PAF#NMC
#PAF#NIF#DESJUD --> #PAF#NMP



#PAF
#PAF#NMP
#PAF#NMP#GABs
#PAF#NMP#ARQ
#PAF#NMC
#PAF#NMC#GABs
#PAF#NMC#ARQ
#PAF#NIF
#PAF#NIF#GABs
#PAF#NIF#ARQ
#PAF#NIF#DESJUD


