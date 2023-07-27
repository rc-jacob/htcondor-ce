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
  subgraph HTCondor-CE %% Subgraph names == Uppercase; node names == lowercase
    direction LR %% Set direction of isolated subgraphs
    A(Job Router) --> B[[CE schedd]]
    B --> C{Grid Mgr.}
    D[(Log)] ---|Log job| C
  end
  subgraph Blahp
    direction LR
    subgraph lsf_*.sh %% Place nested subgraphs above internal nodes
      direction LR
      AA[submit] ---|OR| BB[cancel]
      BB ---|OR| CC[status]
    end
    E[[blahp]] --> lsf_*.sh
    lsf_*.sh -->|args| F[common_sub_attr.sh]
    F -->|attrs| lsf_*.sh
  end
  subgraph Batch Sys
    direction LR
    G((qsub))
  end
  %% - Link nodes and subgraphs here -
  %% - End Links
  %% - External nodes below this point -
  0>Job Ad]
  1[blin.sh]
  %% - End External Nodes
%% -- Body --
```
