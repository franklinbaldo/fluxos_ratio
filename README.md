# fluxos_ratio
# paf


```mermaid
flowchart LR


subgraph cdist
  CDIST((CDIST))
end

subgraph pge
  PAF-ARQEXE((PAF-ARQEXE))
end

subgraph paf
  #PAF
  
  subgraph nmp
    #PAF#NMP
    #PAF#NMP#GABs
    #PAF#NMP#ARQ
  end
  subgraph nmc
    #PAF#NMC
    #PAF#NMC#GABs
    #PAF#NMC#ARQ
  end
  subgraph nif
    #PAF#NIF
    #PAF#NIF#GABs
    
    subgraph desjud
      #PAF#NIF#DESJUD
    end
    #PAF#NIF#ARQ
   end
end

CDIST <--> #PAF


#PAF <--> #PAF#NMP
#PAF <--> #PAF#NMC
#PAF <--> #PAF#NIF


#PAF#NMP <--> #PAF#NMP#GABs --> #PAF#NMP#ARQ --> #PAF#NMP
#PAF#NMP#GABs --> #PAF#NMC#ARQ & #PAF#NIF

#PAF#NMC --> #PAF#NMC#GABs <--> #PAF#NMC#ARQ --> #PAF#NMC
#PAF#NMC#GABs --> #PAF#NMP#ARQ & #PAF#NIF

#PAF#NIF --> #PAF#NIF#GABs <--> #PAF#NIF#ARQ --> #PAF#NIF
#PAF#NIF#GABs --> #PAF#NMP & #PAF#NMC

#PAF#NIF <--> #PAF#NIF#DESJUD --> #PAF#NMC & #PAF#NMP & PAF-ARQEXE

#PAF#NIF & #PAF#NMP & #PAF#NMC --> PAF-ARQEXE





