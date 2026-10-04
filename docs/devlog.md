## 2026-10-03

- Estudei: Missing Semester aula 2 (Shell Tools and Scripting) + exercícios oficiais 1-5 completos
- Pratiquei: ls com flags combinadas, funções bash (marco/polo), command substitution $(), variáveis globais entre funções, while como teste de comando, stdout/stderr separados ($?, >&2, redirecionamento duplo), contador com (( var++ )), find -name/-print0, xargs --null, zip, find -printf com %T@, sort -nr
- Travei em: chmod +X (maiúsculo) não é igual a +x; $? sozinho não é um teste, bash tenta executá-lo como comando; find "*.html" sem -name busca nome literal; erro de digitação (hmtl vs html)
- Resolvi: revisão completa de stdout/stderr e exit codes; usei (( var++ )) para contador dentro do while; find -name "*.html" -print0 + xargs --null para lidar com espaços; find -printf '%T@ %p\n' + sort -nr + head -1 para achar arquivo mais recente

## 2026-10-0X

- Estudei: Missing Semester aula 3 (Editors/Vim), exercícios 1-6 oficiais completos
- Pratiquei: vimtutor, .vimrc (set number, syntax on, tabstop, expandtab), navegação hjkl/w/b/0/$/gg/G, edição dd/yy/p/x/u, VSCodeVim, substituição :s com regex e grupos de captura \(\) \1, J para juntar linhas, macros qa/@a/@@
- Travei em: cursor desalinhado ao combinar k k + J dentro da macro gravada, causando junção de linhas erradas
- Resolvi: refiz passo a passo sem macro, conferindo a posição do cursor com :echo line(".") antes de cada J, até validar a lógica manualmente
