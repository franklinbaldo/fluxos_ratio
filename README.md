# fluxos_ratio
# paf


```mermaid
flowchart LR


subgraph cdist
  CDIST((CDIST))
end

subgraph arquivos
  PAF-ARQEXE((PAF-ARQEXE))
  #PAF#NIF#ARQ
  #PAF#NMC#ARQ
  #PAF#NMP#ARQ
end

subgraph paf
  #PAF
  
  subgraph nmp
    #PAF#NMP((#PAF#NMP))
    #PAF#NMP#GABs
    
  end
  subgraph nmc
    #PAF#NMC((#PAF#NMC))
    #PAF#NMC#GABs
    
  end
  subgraph nif
    #PAF#NIF((#PAF#NIF))
    #PAF#NIF#GABs
    
    subgraph desjud
      #PAF#NIF#DESJUD
    end
    
   end
end

CDIST <--> #PAF

#PAF <--> #PAF#NMP
#PAF <--> #PAF#NMC
#PAF <--> #PAF#NIF

#PAF#NMP <--> #PAF#NMP#GABs --> arquivos 
#PAF#NMP#ARQ --> #PAF#NMP
#PAF#NMP#GABs --> nif
#PAF#NMP#GABs --> NMP

#PAF#NMC --> #PAF#NMC#GABs --> arquivos --> #PAF#NMC
#PAF#NMC#ARQ --> #PAF#NMC
#PAF#NMC#GABs --> nif
#PAF#NMC#GABs --> nmp

#PAF#NIF --> #PAF#NIF#GABs --> arquivos --> #PAF#NIF
#PAF#NIF#ARQ --> #PAF#NIF
#PAF#NIF#GABs --> nmc
#PAF#NIF#GABs --> nmp

#PAF#NIF --> #PAF#NIF#DESJUD --> arquivos
#PAF#NIF#DESJUD --> nmp
#PAF#NIF#DESJUD --> nmc

#PAF#NIF#GABs & #PAF#NMP#GABs & #PAF#NMC#GABs --> PAF-ARQEXE





