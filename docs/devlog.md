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

## 2026-10-10

- Estudei: Missing Semester aula 4 (Data Wrangling), exercícios 1-3 oficiais completos
- Pratiquei: regexone.com (regex básico), sed substituicao s/.../.../, sed -i (edicao in-place), perigo do redirecionamento > no mesmo arquivo de entrada, regex com repeticao de grupos (.*a.*a.*a), grep -v para exclusao, grep -oE para extrair so o match, sort | uniq -c | sort -rn para contagem e ranking
- Travei em: regex com espacos literais por engano; aspas simples vs duplas ao incluir apostrofo no padrao; confundi exercicios do regexone.com com os exercicios oficiais da aula (fontes diferentes, numeracao diferente)
- Resolvi: sed -i para edicao segura in-place; troquei aspas externas para duplas para liberar o apostrofo dentro do padrao; separei claramente as duas fontes de exercicios

## 2026-10-06 (parte 2)

- Estudei: Missing Semester aula 4 (Data Wrangling), exercicio 6 completo (dataset real)
- Pratiquei: curl para baixar CSV real (OWID covid data, 16MB), awk -F para separador customizado, awk NR > 1 para pular cabecalho, awk BEGIN/END com variaveis acumuladoras, comparacao condicional para min/max em awk, soma condicional ignorando campos vazios
- Travei em: nao sabia a sintaxe de acumular soma em awk (vim de bash com (( var++ )), awk usa var = var + algo)
- Resolvi: montei a logica com duas regras separadas (uma por coluna) mais bloco END, awk trata variavel nao inicializada como 0 para soma, diferente do caso de min/max que precisa checar vazio explicitamente
