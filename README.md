Destinado a manter o repositório local dos containers docker para projeto simtx

Necessário criar um aquivo chamado .env e colocar no mesmo diretório do docker_compose.yml com os seguintes parametros:

# ------------ Definicao path dos fontes -------------
DEVOPS_ARRECADACAO_PATH=/C/devtools/git/git_devops 
DEVOPS_PAGAMENTOPIX_PATH=/C/devtools/git/git_devops
DEVOPS_AGENDAMENTOPIX_PATH=/C/devtools/git/git_devops
FONTES_DES_CAIXA_SIMTX_PATH=/C/devtools/git/git_caixa 
FONTES_DES_CAIXA_SICCO_PATH=/C/devtools/git/git_caixa
SIMULADOR_REST=/C/devtools/git/git_hub/simtx-simulador
SIMULADOR_MQ=/C/devtools/git/git_stefanini/simulador-mq
# ---------- Definicao de portas ---------------
PORTA_SICCO=                38080:8080
PORTA_SICCO_DEBUG=          38787:8787
PORTA_SIMTX=                28080:8080
PORTA_SIMTX_DEBUG=          28787:8787
PORTA_PAGAMENTOPIX=         48080:8080
PORTA_PAGAMENTOPIX_DEBUG=   48787:8787
PORTA_SIMULADOR_REST=       58080:8080
PORTA_SIMULADOR_REST_DEBUG= 58787:8787
PORTA_PEC=                  18080:8080
PORTA_PEC_DEBUG=            18787:8787
PORTA_AGENDAMENTO=          28081:8080
PORTA_AGENDAMENTO_DEBUG=    28788:8787
PORTA_DESFAZIMENTO=         18081:8080
PORTA_DESFAZIMENTO_DEBUG=   18788:8787
PORTA_SIMULADOR_MQ=         28086:8080
 
 OBS: Os valores dos parametros devem ser apontados para o caminho da máquina do usuário.