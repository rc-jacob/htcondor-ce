CE Overview
===
```mermaid
%% -- HEADER ---
flowchart LR %% Specify diagram type ('flowchart') and direction ('LR' == Left-Right)
%% -- HEADER --

%% -- BODY --
  subgraph HTCondor-CE
    direction LR %% Set direction of isolated subgraphs
  end

  subgraph Blahp %% Subgraph names == Uppercase; node names == lowercase
    direction LR
  end

  subgraph Batch Sys
    direction LR
  end

%% - External nodes below this point -
  0>Job Ad] 
%% -- Body --
```
