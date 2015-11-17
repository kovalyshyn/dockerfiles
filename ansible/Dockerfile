from debian:jessie

add ./playbooks /playbooks
add ./entrypoint.sh /entrypoint.sh
run apt-get update && \
    apt-get install -y ansible ssh && \
    chmod +x /entrypoint.sh && \
    rm -rf /var/lib/apt/lists/*
add ./conf/ansible.cfg /etc/ansible/ansible.cfg

entrypoint ["./entrypoint.sh"]
cmd ["/playbooks/bootstrap.yml"]
