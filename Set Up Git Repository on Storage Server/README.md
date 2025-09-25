# Set Up Git Repository on Storage Server

The Nautilus development team has provided requirements to the DevOps team for a new application development project, specifically requesting the establishment of a Git repository. Follow the instructions below to create the Git repository on the `Storage server` in the Stratos DC:

Utilize yum to install the git package on the `Storage Server`.

Create a bare repository named `/opt/games.git` (ensure exact name usage).

## 1. Install Git on Storage Server

`ssh natasha@ststor01`

`sudo -s`

`hostnamectl`

```console
 Static hostname: ststor01.stratos.xfusioncorp.com
       Icon name: computer-container
         Chassis: container ☐
      Machine ID: ce131cf36c8149f9a5285064fd7c61a0
         Boot ID: 65dc3786ac2c47909622a5ecd15eb622
  Virtualization: docker
Operating System: CentOS Stream 9                 
     CPE OS Name: cpe:/o:centos:centos:9
          Kernel: Linux 5.4.0-1106-gcp
    Architecture: x86-64
Firmware Version: Google
```

`yum install -y git`

```console
Installed:
  emacs-filesystem-1:27.2-18.el9.noarch                                        
  git-2.47.3-1.el9.x86_64                                                      
  git-core-2.47.3-1.el9.x86_64                                                 
  git-core-doc-2.47.3-1.el9.noarch                                             
  groff-base-1.22.4-10.el9.x86_64                                              
  less-590-6.el9.x86_64                                                        
  perl-AutoLoader-5.74-483.el9.noarch                                          
  perl-B-1.80-483.el9.x86_64                                                   
  perl-Carp-1.50-460.el9.noarch                                                
  perl-Class-Struct-0.66-483.el9.noarch                                        
  perl-Data-Dumper-2.174-462.el9.x86_64                                        
  perl-Digest-1.19-4.el9.noarch                                                
  perl-Digest-MD5-2.58-4.el9.x86_64                                            
  perl-DynaLoader-1.47-483.el9.x86_64                                          
  perl-Encode-4:3.08-462.el9.x86_64                                            
  perl-Errno-1.30-483.el9.x86_64                                               
  perl-Error-1:0.17029-7.el9.noarch                                            
  perl-Exporter-5.74-461.el9.noarch                                            
  perl-Fcntl-1.13-483.el9.x86_64                                               
  perl-File-Basename-2.85-483.el9.noarch                                       
  perl-File-Find-1.37-483.el9.noarch                                           
  perl-File-Path-2.18-4.el9.noarch                                             
  perl-File-Temp-1:0.231.100-4.el9.noarch                                      
  perl-File-stat-1.09-483.el9.noarch                                           
  perl-FileHandle-2.03-483.el9.noarch                                          
  perl-Getopt-Long-1:2.52-4.el9.noarch                                         
  perl-Getopt-Std-1.12-483.el9.noarch                                          
  perl-Git-2.47.3-1.el9.noarch                                                 
  perl-HTTP-Tiny-0.076-462.el9.noarch                                          
  perl-IO-1.43-483.el9.x86_64                                                  
  perl-IO-Socket-IP-0.41-5.el9.noarch                                          
  perl-IO-Socket-SSL-2.073-2.el9.noarch                                        
  perl-IPC-Open3-1.21-483.el9.noarch                                           
  perl-MIME-Base64-3.16-4.el9.x86_64                                           
  perl-Mozilla-CA-20200520-6.el9.noarch                                        
  perl-NDBM_File-1.15-483.el9.x86_64                                           
  perl-Net-SSLeay-1.94-3.el9.x86_64                                            
  perl-POSIX-1.94-483.el9.x86_64                                               
  perl-PathTools-3.78-461.el9.x86_64                                           
  perl-Pod-Escapes-1:1.07-460.el9.noarch                                       
  perl-Pod-Perldoc-3.28.01-461.el9.noarch                                      
  perl-Pod-Simple-1:3.42-4.el9.noarch                                          
  perl-Pod-Usage-4:2.01-4.el9.noarch                                           
  perl-Scalar-List-Utils-4:1.56-462.el9.x86_64                                 
  perl-SelectSaver-1.02-483.el9.noarch                                         
  perl-Socket-4:2.031-4.el9.x86_64                                             
  perl-Storable-1:3.21-460.el9.x86_64                                          
  perl-Symbol-1.08-483.el9.noarch                                              
  perl-Term-ANSIColor-5.01-461.el9.noarch                                      
  perl-Term-Cap-1.17-460.el9.noarch                                            
  perl-TermReadKey-2.38-11.el9.x86_64                                          
  perl-Text-ParseWords-3.30-460.el9.noarch                                     
  perl-Text-Tabs+Wrap-2013.0523-460.el9.noarch                                 
  perl-Time-Local-2:1.300-7.el9.noarch                                         
  perl-URI-5.09-3.el9.noarch                                                   
  perl-base-2.27-483.el9.noarch                                                
  perl-constant-1.33-461.el9.noarch                                            
  perl-if-0.60.800-483.el9.noarch                                              
  perl-interpreter-4:5.32.1-483.el9.x86_64                                     
  perl-lib-0.65-483.el9.x86_64                                                 
  perl-libnet-3.13-4.el9.noarch                                                
  perl-libs-4:5.32.1-483.el9.x86_64                                            
  perl-mro-1.23-483.el9.x86_64                                                 
  perl-overload-1.31-483.el9.noarch                                            
  perl-overloading-0.02-483.el9.noarch                                         
  perl-parent-1:0.238-460.el9.noarch                                           
  perl-podlators-1:4.14-460.el9.noarch                                         
  perl-subs-1.03-483.el9.noarch                                                
  perl-vars-1.05-483.el9.noarch                                                

Complete!
```

## 2. Setup user Git config

`git config --global --add user.name natasha`
`git config --global --add user.email natasha@stratos.xfusioncorp.com`

## 3. Create a bare repository

`mkdir -p /opt/games.git && cd $_`
`git init --bare /opt/games.git`

```console
hint: Using 'master' as the name for the initial branch. This default branch name
hint: is subject to change. To configure the initial branch name to use in all
hint: of your new repositories, which will suppress this warning, call:
hint:
hint:   git config --global init.defaultBranch <name>
hint:
hint: Names commonly chosen instead of 'master' are 'main', 'trunk' and
hint: 'development'. The just-created branch can be renamed via this command:
hint:
hint:   git branch -m <name>
Initialized empty Git repository in /opt/games.git/
```

`ls -la`

```console
total 40
drwxr-xr-x 7 root root 4096 Sep 25 20:12 .
drwxr-xr-x 1 root root 4096 Sep 25 20:12 ..
-rw-r--r-- 1 root root   23 Sep 25 20:12 HEAD
drwxr-xr-x 2 root root 4096 Sep 25 20:12 branches
-rw-r--r-- 1 root root   66 Sep 25 20:12 config
-rw-r--r-- 1 root root   73 Sep 25 20:12 description
drwxr-xr-x 2 root root 4096 Sep 25 20:12 hooks
drwxr-xr-x 2 root root 4096 Sep 25 20:12 info
drwxr-xr-x 4 root root 4096 Sep 25 20:12 objects
drwxr-xr-x 4 root root 4096 Sep 25 20:12 refs
```


