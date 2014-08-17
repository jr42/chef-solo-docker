FROM centos:centos7
MAINTAINER jr@runningthematrix.com

RUN yum -y install tar make gcc gcc-c++ perl libxml2-devel libxslt-devel
RUN curl -L https://www.opscode.com/chef/install.sh | bash
RUN echo "gem: --no-ri --no-rdoc" > ~/.gemrc
RUN /opt/chef/embedded/bin/gem install -r berkshelf

RUN yum -y remove perl perl-* *-headers *-devel gcc gcc-c++ tar make
RUN yum clean all


