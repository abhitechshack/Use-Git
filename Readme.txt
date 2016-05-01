****************** Use git on rhel 6.5 *****************

[root@abhiteckshack Desktop]# cat /etc/redhat-release 
Red Hat Enterprise Linux Server release 6.5 (Santiago)
[root@abhiteckshack Desktop]# 

********************************************************

step 1 : Install git on rhel 6.5 ?

[root@abhiteckshack Desktop]# yum install git -y
Loaded plugins: product-id, refresh-packagekit, security, subscription-manager
This system is not registered to Red Hat Subscription Management. You can use subscription-manager to register.
Repository 'linux' is missing name in configuration, using id
Setting up Install Process
Resolving Dependencies
--> Running transaction check
---> Package git.x86_64 0:1.7.1-3.el6_4.1 will be installed
--> Processing Dependency: perl-Git = 1.7.1-3.el6_4.1 for package: git-1.7.1-3.el6_4.1.x86_64
--> Processing Dependency: perl(Git) for package: git-1.7.1-3.el6_4.1.x86_64
--> Processing Dependency: perl(Error) for package: git-1.7.1-3.el6_4.1.x86_64
--> Running transaction check
---> Package perl-Error.noarch 1:0.17015-4.el6 will be installed
---> Package perl-Git.noarch 0:1.7.1-3.el6_4.1 will be installed
--> Finished Dependency Resolution

Dependencies Resolved

================================================================================
 Package            Arch           Version                  Repository     Size
================================================================================
Installing:
 git                x86_64         1.7.1-3.el6_4.1          linux         4.6 M
Installing for dependencies:
 perl-Error         noarch         1:0.17015-4.el6          linux          29 k
 perl-Git           noarch         1.7.1-3.el6_4.1          linux          28 k

Transaction Summary
================================================================================
Install       3 Package(s)

Total download size: 4.7 M
Installed size: 15 M
Downloading Packages:
--------------------------------------------------------------------------------
Total                                            20 MB/s | 4.7 MB     00:00     
Running rpm_check_debug
Running Transaction Test
Transaction Test Succeeded
Running Transaction
  Installing : 1:perl-Error-0.17015-4.el6.noarch                            1/3 
  Installing : perl-Git-1.7.1-3.el6_4.1.noarch                              2/3 
  Installing : git-1.7.1-3.el6_4.1.x86_64                                   3/3 
  Verifying  : git-1.7.1-3.el6_4.1.x86_64                                   1/3 
  Verifying  : perl-Git-1.7.1-3.el6_4.1.noarch                              2/3 
  Verifying  : 1:perl-Error-0.17015-4.el6.noarch                            3/3 

Installed:
  git.x86_64 0:1.7.1-3.el6_4.1                                                  

Dependency Installed:
  perl-Error.noarch 1:0.17015-4.el6      perl-Git.noarch 0:1.7.1-3.el6_4.1     

Complete!
[root@abhiteckshack Desktop]# 




step 2 : Configure user information for all local repositories ?

[root@abhiteckshack Desktop]# git config --global user.name "abhitechshack"
[root@abhiteckshack Desktop]# git config --global user.email "abhitechshack@gmail.com"
[root@abhiteckshack Desktop]# 



step 3 : Start a new repository ?

[root@abhiteckshack Desktop]# git init Use-Git
Initialized empty Git repository in /root/Desktop/Use-Git/.git/
[root@abhiteckshack Desktop]# 
[root@abhiteckshack Desktop]# ls
Use-Git
[root@abhiteckshack Desktop]#


step 4 : create file or folders in Use-Git folder ?

[root@abhiteckshack Use-Git]# ls
Redme.md
[root@abhiteckshack Use-Git]#


step 5 : add those file and folder in git (Snapshots the file in preparation for versioning) ?

[root@abhiteckshack Use-Git]# git add Redme.md 
[root@abhiteckshack Use-Git]#



step 6 : check the git status ?


[root@abhiteckshack Use-Git]# git status
# On branch master
#
# Initial commit
#
# Changes to be committed:
#   (use "git rm --cached <file>..." to unstage)
#
#	new file:   Redme.md
#
[root@abhiteckshack Use-Git]# 




step 7 : give a message on that file/folder which we have created (Records file snapshots permanently in version history) ?


[root@abhiteckshack Use-Git]# git commit -m "file shows how i use GIT"
[master (root-commit) 164c1c7] file shows how i use GIT
 1 files changed, 79 insertions(+), 0 deletions(-)
 create mode 100644 Redme.md
[root@abhiteckshack Use-Git]# 


step 8 : add our file/folder on GitHub ?

[root@abhiteckshack Use-Git]# git remote set-url origin https://abhitechshack@github.com/abhitechshack/Use-Git.git
[root@abhiteckshack Use-Git]# 



step 9 : Now push our file/folder on GitHub ?

[root@abhiteckshack Use-Git]# git push -u  origin master
Counting objects: 3, done.
Delta compression using up to 2 threads.
Compressing objects: 100% (2/2), done.
Writing objects: 100% (3/3), 1.56 KiB, done.
Total 3 (delta 0), reused 0 (delta 0)
To https://abhitechshack@github.com/abhitechshack/Use-Git.git
 * [new branch]      master -> master
Branch master set up to track remote branch master from origin.
[root@abhiteckshack Use-Git]#
