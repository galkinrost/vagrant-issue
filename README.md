# vagrant-issue

The following SSH command responded with a non-zero exit status.
Vagrant assumes that this means the command failed!
 
 
          rm -f /var/lib/vagrant/cids/c90d99e12e1feb571c017a62a7c5a4500c9fd495
          docker run --cidfile=/var/lib/vagrant/cids/c90d99e12e1feb571c017a62a7c5a4500c9fd495 -d --name postgres postgres
 
 
Stdout from the command:
 
6f30920500bc0efe5a62e111f9daac18090e28288a4ca666b3ea28a035cdccee
 
 
Stderr from the command:
 
stdin: is not a tty
2014/10/08 16:14:33 Error response from daemon: Cannot start container 6f30920500bc0efe5a62e111f9daac18090e28288a4ca666b3ea28a035cdccee: no such file or directory
