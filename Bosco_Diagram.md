Bosco Overview
===
```mermaid
flowchart LR
	subgraph Bosco
		direction LR
		1[Schedd] --> 2[Grid</br>Manager]
		3[SP] --> 2
		2 --- 4[SSH]
    2 --- 5[SSH]
		5 --> |FTP|2
		3 -. Data Channel .- 5
	end
	subgraph Remote Submit
		direction LR
		a[sshd] --> b[blahp]
		c[sshd] --> d[FTGahp]
		d -. SSH Tunnel .- c
		e[OSG] --> f[osg/rdo-null]
	end
id1[(FTP)]
```
