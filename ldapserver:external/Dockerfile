# Version: 0.0.1
# @edt M06 2018-2019
# ldapserver base edt.org
# -------------------------------------
FROM fedora:27
LABEL author="@edt ASIX M06 Curs 2018-2019"
LABEL description="ldapserver edt.org cn dataDB"
RUN dnf -y install procps openldap-clients openldap-servers vim passwd cyrus-sasl-ldap cyrus-sasl
RUN mkdir /opt/docker
COPY * /opt/docker/
RUN chmod +x /opt/docker/*.sh /opt/docker/startup.sh
WORKDIR /opt/docker
EXPOSE 389 636
CMD ["/opt/docker/startup.sh"]
