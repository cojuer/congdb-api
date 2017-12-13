## Fdmpd project

### Prerequisites
libnl-genl-3-dev

### Installation
mkdir build  
cd build  
cmake ../  
make  
make install  

### Usage
Project installs two binary files:  
fdmpd - daemon, that connects to the kernel part of fdmp and 
controls it using range of heuristics.  
fdmp-ctl - command line tool to explicitly show/change fdmp 
kernel part configuration.  
  
