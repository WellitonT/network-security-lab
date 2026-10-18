# Network Security Lab

Laboratório de hardening defensivo de infraestrutura Linux. O foco é configurar e proteger um servidor como um administrador de sistemas faria, documentando cada decisão. Não inclui ferramentas ofensivas.

## Ambiente

- Servidor: VM **Rocky Linux 9** no VirtualBox, rede NAT
- Cliente: Windows, acessando por SSH via redirecionamento de porta
- Acesso configurado por alias no `~/.ssh/config`

## O que já foi feito

**Hardening do SSH**

- Autenticação por chave **ed25519** com passphrase
- `PasswordAuthentication no`: login por senha desativado
- `PermitRootLogin no`: login direto como root bloqueado

**Firewall**

- `firewalld` ativo, com o serviço `ssh` liberado

**Ambiente de trabalho**

- Prática de shell scripting, Vim, tmux e controle de jobs
- Dotfiles versionados em [github.com/WellitonT/dotfiles](https://github.com/WellitonT/dotfiles)

## Escopo planejado

- Baseline de firewall documentado e reproduzível
- Scripts de monitoramento e healthcheck
- Automação da configuração (hoje manual)

Itens desta lista ainda **não** estão implementados.

## Princípios

- **Defensivo apenas:** o objetivo é reduzir superfície de ataque, não explorá-la.
- **Reprodutível:** cada configuração deve poder ser refeita a partir da documentação.
- **Sem segredos no repositório:** chaves privadas e senhas nunca são versionadas.

## Autor

Welliton ([LinkedIn](https://www.linkedin.com/in/welliton-tiene-336bb7207/)) · trilha autodidata em infraestrutura, rumo a DevOps e MLOps.
