# fluxos_ratio
# paf


```mermaid
flowchart LR


subgraph cdist
  CDIST((CDIST))
end



subgraph paf
  #PAF((#PAF))
  PAF-ARQEXEPAF-ARQEXE
  
  subgraph nmp
    #PAF#NMP((#PAF#NMP))
    #PAF#NMP#GABs
    #PAF#NMP#ARQ
  end
  subgraph nmc
    #PAF#NMC((#PAF#NMC))
    #PAF#NMC#GABs
    #PAF#NMC#ARQ
  end
  subgraph nif
    #PAF#NIF((#PAF#NIF))
    #PAF#NIF#GABs
    #PAF#NIF#ARQ
    subgraph desjud
      #PAF#NIF#DESJUD
    end
    
   end
end

CDIST --> #PAF
#PAF --> CDIST

#PAF --> nmp
#PAF --> nmc
#PAF --> nif

#PAF#NMP --> #PAF#NMP#GABs --> #PAF#NMP#ARQ --> #PAF#NMP
#PAF#NMP#GABs --> #PAF#NMP
#PAF#NMP#GABs --> nif
#PAF#NMP#GABs --> nmc

#PAF#NMC --> #PAF#NMC#GABs --> #PAF#NMC#ARQ --> #PAF#NMC
#PAF#NMC#GABs --> #PAF#NMC
#PAF#NMC#GABs --> nif
#PAF#NMC#GABs --> nmp

#PAF#NIF --> #PAF#NIF#GABs --> #PAF#NIF#ARQ --> #PAF#NIF
#PAF#NIF#GABs --> #PAF#NIF
#PAF#NIF#GABs --> nmc
#PAF#NIF#GABs --> nmp

#PAF#NIF --> #PAF#NIF#DESJUD --> PAF-ARQEXE
#PAF#NIF#DESJUD --> nmp
#PAF#NIF#DESJUD --> nmc

PAF-ARQEXE --> #PAF






