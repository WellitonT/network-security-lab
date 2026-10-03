## 2026-10-03

- Estudei: Missing Semester aula 2 (Shell Tools and Scripting) + exercícios oficiais 1-5 completos
- Pratiquei: ls com flags combinadas, funções bash (marco/polo), command substitution $(), variáveis globais entre funções, while como teste de comando, stdout/stderr separados ($?, >&2, redirecionamento duplo), contador com (( var++ )), find -name/-print0, xargs --null, zip, find -printf com %T@, sort -nr
- Travei em: chmod +X (maiúsculo) não é igual a +x; $? sozinho não é um teste, bash tenta executá-lo como comando; find "*.html" sem -name busca nome literal; erro de digitação (hmtl vs html)
- Resolvi: revisão completa de stdout/stderr e exit codes; usei (( var++ )) para contador dentro do while; find -name "*.html" -print0 + xargs --null para lidar com espaços; find -printf '%T@ %p\n' + sort -nr + head -1 para achar arquivo mais recente
