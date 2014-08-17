FROM centos:centos6
MAINTAINER jr@runningthematrix.com

ONBUILD yum -y install tar gcc gcc-c++ perl libxml2-devel libxslt-devel
ONBUILD curl -L https://www.opscode.com/chef/install.sh | bash
ONBUILD echo "gem: --no-ri --no-rdoc" > ~/.gemrc
ONBUILD /opt/chef/embedded/bin/gem install -r berkshelf

ONBUILD yum -y remove perl perl-* *-headers *-devel gcc gcc-c++ tar 
ONBUILD yum clean all


