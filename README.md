# Network Security Lab

Laboratório de estudo de administração e hardening de um servidor Linux em máquina virtual.

## Ambiente

- Máquina virtual: Oracle VirtualBox
- Sistema do servidor: Ubuntu

## O que foi feito

- Acesso SSH somente por chave ed25519
- Login por senha desativado
- Login direto como root desativado
- Atalhos de conexão em `~/.ssh/config`
- Registro de cada sessão em `devlog.md`

## Como verificar

No servidor, confira a configuração em vigor:

```bash
sudo sshd -T | grep -Ei 'passwordauthentication|permitrootlogin|pubkeyauthentication'
```

Resultado esperado: `passwordauthentication no`, `permitrootlogin no` e `pubkeyauthentication yes`.

## Em andamento

- Baseline de firewall
- Scripts de monitoramento e healthcheck
