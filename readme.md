#readme

###安装ansible
pip install  git+https://github.com/edx/ansible.git@stable-1.9.3-rc1-edx#egg=ansible==1.9.3-edx

###配置


###安装
*  git clone https://github.com/edx/configuration
*  cd /var/tmp/configuration
*  git checkout named-release/dogwood.rc
*  sed -i "/COMMON_SSH_PASSWORD_AUTH/c COMMON_SSH_PASSWORD_AUTH: \"yes\"" playbooks/roles/common/defaults/main.yml
*  sudo ansible-playbook -c local ./edx_sandbox.yml -i "localhost," -e 'edx_platform_version=named-release/dogwood.rc certs_version=named-release/dogwood.rc forum_version=named-release/dogwood.rc xqueue_version=named-release/dogwood.rc'


