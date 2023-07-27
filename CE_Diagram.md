CE Overview
===
```mermaid
%% -- HEADER ---
  %% Keep all diagram information, including directives,
  %% within the header limits
flowchart LR %% Specify diagram type ('flowchart') and direction ('LR' == Left-Right)
%% -- HEADER --
%% -- BODY --
  %% External nodes are numbered (0 - 100)
  %% Internal nodes are alphabetic (A - Z)
  %% Nodes within nested subgraphs labeled
  %% by double letters (AA - ZZ)
  subgraph HTCondor-CE
    direction LR %% Set direction of isolated subgraphs
    A(Job Router) --> B[[CE schedd]]
    B --> C{Grid Mgr.}
    D[(Log)] ---|Log job| C
  end
  subgraph Blahp %% Subgraph names == Uppercase; node names == lowercase
    direction LR
  end
  subgraph Batch Sys
    direction LR
  end
  %% - Link nodes and subgraphs here -
  %% - End Links
  %% - External nodes below this point -
  0>Job Ad]
  %% - End External Nodes
%% -- Body --
```
