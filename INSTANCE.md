## Instance Inspection
Instructions:
  - Install dive on MacOS: `brew install dive`
  - Run `dive image-tag:version` such as `dive amitkumarjaiswal/rl:latest`

Here is an example:

```
1465 ◯  docker pull amitkumarjaiswal/rl
Using default tag: latest
latest: Pulling from amitkumarjaiswal/rl
f7277927d38a: Pull complete 
8d3eac894db4: Pull complete 
edf72af6d627: Pull complete 
3e4f86211d23: Pull complete 
95bb815ded09: Pull complete 
f342db953b79: Pull complete 
4e55618eec1b: Pull complete 
d27e9c06372c: Pull complete 
1fc1afcf36bb: Pull complete 
741ec026e7fe: Pull complete 
b3c2ede4b6d9: Pull complete 
1ef635721fd2: Pull complete 
06cde93c335c: Pull complete 
5bd67bff14c9: Pull complete 
a2f57573a5f7: Pull complete 
78e6f1937b06: Pull complete 
2c66d7334c67: Pull complete 
b4f63aaf7e64: Pull complete 
Digest: sha256:1b93ff820d1c4360eadd80ee162f52da8862a11ec2c43b37cd7f1da2e059ec1d
Status: Downloaded newer image for amitkumarjaiswal/rl:latest
docker.io/amitkumarjaiswal/rl:latest
pc-138-111 ॐ  ~:
1466 ◯  dive -v
dive 0.9.2
pc-138-111 ॐ  ~:
1467 ◯  dive amitkumarjaiswal/rl:latest
Image Source: docker://amitkumarjaiswal/rl:latest
Fetching image... (this can take a while for large images)
Analyzing image...
Building cache...

┃ ● Layers ┣━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ │ Current Layer Contents ├────────────────────────────────────────────────────────────────────────────────────────────
Cmp   Size  Command                                                                                                    Permission     UID:GID       Size  Filetree
    120 MB  FROM e31c06a18fd79ea                                                                                       drwxr-xr-x         0:0     7.4 MB  ├── bin
       0 B  rm -rf /var/lib/apt/lists/*                                                                                -rwxr-xr-x         0:0     1.0 MB  │   ├── bash
     745 B  set -xe   && echo '#!/bin/sh' > /usr/sbin/policy-rc.d  && echo 'exit 101' >> /usr/sbin/policy-rc.d  && chm -rwxr-xr-x         0:0      52 kB  │   ├── cat    
       7 B  mkdir -p /run/systemd && echo 'docker' > /run/systemd/container                                            -rwxr-xr-x         0:0      60 kB  │   ├── chgrp              
    268 MB  apt-get update && apt-get install -y -qq   build-essential   wget vim  module-init-tools > /dev/null       -rwxr-xr-x         0:0      56 kB  │   ├── chmod         
    4.2 GB  cd /tmp &&     wget https://developer.nvidia.com/compute/cuda/10.0/Prod/local_installers/cuda_10.0.130_410 -rwxr-xr-x         0:0      64 kB  │   ├── chown 
      22 B  #(nop) ADD file:92358d0237f4fab799820b7220e08f8d709e0af471a0c0f239dd37aea8dcd921 in /etc/ld.so.conf.d      -rwxr-xr-x         0:0     151 kB  │   ├── cp              
     34 kB  ldconfig -v                                                                                                -rwxr-xr-x         0:0     154 kB  │   ├── dash 
       0 B  mkdir /work /common                                                                                        -rwxr-xr-x         0:0      68 kB  │   ├── date            
    7.5 MB  DEBIAN_FRONTEND=noninteractive apt-get update                                                              -rwxr-xr-x         0:0      73 kB  │   ├── dd    
    328 MB  apt install -y --no-install-recommends     build-essential cmake     apt-utils     libopenblas-dev     pyt -rwxr-xr-x         0:0      98 kB  │   ├── df                 
     10 MB  apt-get install -y --no-install-recommends libjpeg-dev zlib1g-dev &&     pip3 --no-cache-dir install 'pill -rwxr-xr-x         0:0     127 kB  │   ├── dir         
    410 MB  pip3 --no-cache-dir install     numpy pandas sympy scipy sklearn scikit-image matplotlib requests          -rwxr-xr-x         0:0      61 kB  │   ├── dmesg          
    1.4 GB  pip3 --no-cache-dir install 'torchvision==0.6.0' 'torch==1.5.0' torchsummary 'networkx==2.0'               -rwxrwxrwx         0:0        0 B  │   ├── dnsdomainname → hostname
    9.4 MB  pip3 install tensorboardX                                                                                  -rwxrwxrwx         0:0        0 B  │   ├── domainname → hostname
    1.4 GB  pip3 install --no-cache-dir --upgrade tensorflow                                                           -rwxr-xr-x         0:0      31 kB  │   ├── echo 
    3.9 MB  pip3 install --no-cache-dir --upgrade pydot_ng keras                                                       -rwxr-xr-x         0:0       28 B  │   ├── egrep
     17 MB  pip3 install gym && pip install --upgrade pip                                                              -rwxr-xr-x         0:0      27 kB  │   ├── false
                                                                                                                       -rwxr-xr-x         0:0       28 B  │   ├── fgrep
│ Layer Details ├───────────────────────────────────────────────────────────────────────────────────────────────────── -rwxr-xr-x         0:0      50 kB  │   ├── findmnt
                                                                                                                       -rwxr-xr-x         0:0     211 kB  │   ├── grep
Tags:   (unavailable)                                                                                                  -rwxr-xr-x         0:0     2.3 kB  │   ├── gunzip
Id:     e31c06a18fd79ea6fd5f42cb878d0c62eeafd12292fc5a8906a2501ec7080db7                                               -rwxr-xr-x         0:0     5.9 kB  │   ├── gzexe
Digest: sha256:f749b9b0fb213e9897417a985aaa9753d41bff474e1d0c0d1d266c4512eaf031                                        -rwxr-xr-x         0:0      98 kB  │   ├── gzip
Command:                                                                                                               -rwxr-xr-x         0:0      15 kB  │   ├── hostname
#(nop) ADD file:603693e48cdc7f0c5c62119923aadbb266e5df5a5002fc0f61295858f91690e8 in /                                  -rwxr-xr-x         0:0     499 kB  │   ├── journalctl              
                                                                                                                       -rwxr-xr-x         0:0      23 kB  │   ├── kill                 
│ Image Details ├───────────────────────────────────────────────────────────────────────────────────────────────────── -rwxr-xr-x         0:0      56 kB  │   ├── ln  
                                                                                                                       -rwxr-xr-x         0:0      48 kB  │   ├── login
                                                                                                                       -rwxr-xr-x         0:0     454 kB  │   ├── loginctl
Total Image size: 8.2 GB                                                                                               -rwxr-xr-x         0:0     127 kB  │   ├── ls   
Potential wasted space: 310 MB                                                                                         -rwxr-xr-x         0:0      77 kB  │   ├── lsblk  
Image efficiency score: 97 %                                                                                           -rwxr-xr-x         0:0      77 kB  │   ├── mkdir
                                                                                                                       -rwxr-xr-x         0:0      64 kB  │   ├── mknod 
Count   Total Space  Path                                                                                              -rwxr-xr-x         0:0      40 kB  │   ├── mktemp
    2         45 MB  /usr/lib/gcc/x86_64-linux-gnu/5/cc1plus                                                           -rwxr-xr-x         0:0      40 kB  │   ├── more
    2         42 MB  /usr/lib/gcc/x86_64-linux-gnu/5/cc1                                                               -rwxr-xr-x         0:0      40 kB  │   ├── mount   
    2         40 MB  /usr/lib/gcc/x86_64-linux-gnu/5/lto1                                                              -rwxr-xr-x         0:0      15 kB  │   ├── mountpoint
    2         11 MB  /usr/lib/gcc/x86_64-linux-gnu/5/libstdc++.a                                                       -rwxr-xr-x         0:0     130 kB  │   ├── mv        
    2        9.1 MB  /usr/lib/x86_64-linux-gnu/libpython3.5m.so.1.0                                                    -rwxr-xr-x         0:0     678 kB  │   ├── networkctl
    2        7.2 MB  /var/lib/apt/lists/archive.ubuntu.com_ubuntu_dists_xenial_main_binary-amd64_Packages              -rwxrwxrwx         0:0        0 B  │   ├── nisdomainname → hostname
    2        6.8 MB  /var/lib/apt/lists/archive.ubuntu.com_ubuntu_dists_xenial-updates_main_binary-amd64_Packages      -rwxrwxrwx         0:0        0 B  │   ├── pidof → /sbin/killall5
    2        6.1 MB  /usr/lib/gcc/x86_64-linux-gnu/5/libgcc.a                                                          -rwxr-xr-x         0:0      97 kB  │   ├── ps   
    2        5.9 MB  /var/lib/apt/lists/archive.ubuntu.com_ubuntu_dists_xenial-updates_main_i18n_Translation-en        -rwxr-xr-x         0:0      32 kB  │   ├── pwd     
    2        4.9 MB  /var/lib/apt/lists/security.ubuntu.com_ubuntu_dists_xenial-security_main_binary-amd64_Packages    -rwxrwxrwx         0:0        0 B  │   ├── rbash → bash
    2        4.8 MB  /var/lib/apt/lists/security.ubuntu.com_ubuntu_dists_xenial-security_main_i18n_Translation-en      -rwxr-xr-x         0:0      40 kB  │   ├── readlink
    2        4.5 MB  /var/lib/apt/lists/archive.ubuntu.com_ubuntu_dists_xenial-updates_main_binary-amd64_Packages.lz4  -rwxr-xr-x         0:0      60 kB  │   ├── rm          
    2        4.3 MB  /usr/lib/gcc/x86_64-linux-gnu/5/libasan.a                                                         -rwxr-xr-x         0:0      40 kB  │   ├── rmdir
    2        3.7 MB  /usr/lib/gcc/x86_64-linux-gnu/5/libtsan.a                                                         -rwxr-xr-x         0:0      19 kB  │   ├── run-parts
    2        3.6 MB  /var/lib/apt/lists/archive.ubuntu.com_ubuntu_dists_xenial_main_i18n_Translation-en                -rwxr-xr-x         0:0      73 kB  │   ├── sed   
    2        3.3 MB  /var/lib/apt/lists/security.ubuntu.com_ubuntu_dists_xenial-security_main_binary-amd64_Packages.lz -rwxrwxrwx         0:0        0 B  │   ├── sh → dash
4                                                                                                                      -rwxrwxrwx         0:0        0 B  │   ├── sh.distrib → dash
    2        3.2 MB  /var/lib/apt/lists/archive.ubuntu.com_ubuntu_dists_xenial-updates_universe_binary-amd64_Packages. -rwxr-xr-x         0:0      31 kB  │   ├── sleep     
lz4                                                                                                                    -rwxr-xr-x         0:0      72 kB  │   ├── stty
    2        3.1 MB  /usr/lib/x86_64-linux-gnu/libstdc++.so.6.0.21                                                     -rwxr-xr-x         0:0      40 kB  │   ├── su        
    2        2.0 MB  /usr/lib/x86_64-linux-gnu/libasan.so.2.0.0                                                        -rwxr-xr-x         0:0      31 kB  │   ├── sync                    
    2        1.9 MB  /var/lib/apt/lists/security.ubuntu.com_ubuntu_dists_xenial-security_universe_binary-amd64_Package -rwxr-xr-x         0:0     664 kB  │   ├── systemctl             
s.lz4                                                                                                                  -rwxrwxrwx         0:0        0 B  │   ├── systemd → /lib/systemd/systemd
    4        1.9 MB  /var/cache/debconf/templates.dat                                                                  -rwxr-xr-x         0:0      52 kB  │   ├── systemd-ask-password
    2        1.8 MB  /usr/bin/cpp-5                                                                                    -rwxr-xr-x         0:0      39 kB  │   ├── systemd-escape
```    
