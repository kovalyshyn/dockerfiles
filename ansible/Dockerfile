from debian:jessie

add ./playbooks /playbooks
add ./conf/ansible.cfg /etc/ansible/ansible.cfg
add ./entrypoint.sh /entrypoint.sh

run apt-get update && \
    apt-get install -y ansible ssh && \
    chmod +x /entrypoint.sh && \
    rm -rf /var/lib/apt/lists/*

entrypoint ["./entrypoint.sh"]
cmd ["/playbooks/bootstrap.yml"]
