# Guia: Criando uma Máquina Virtual no Azure

Este guia cobre as etapas essenciais para criar uma máquina virtual no Azure via Portal, conforme os tópicos do exame AZ-104.

## Etapa 1: Criar Grupo de Recursos

1. Acesse https://portal.azure.com
2. Pesquise por “Grupos de Recursos”
3. Clique em “Criar”
4. Defina um nome como `rg-az104-lab` e escolha uma região

## Etapa 2: Criar Máquina Virtual

1. Vá em “Máquinas Virtuais” > “Criar”
2. Preencha os dados:
   - Nome: `vm-az104-lab`
   - Região: `Brazil South`
   - Imagem: `Ubuntu 20.04 LTS`
   - Tamanho: `Standard_B1s`
   - Autenticação: `Chave pública SSH`
3. Crie um par de chaves (ou use existente)
4. Ative IP público
5. Deixe portas padrão liberadas (SSH)

## Etapa 3: Validar Criação

1. Acesse a aba “Visão Geral” da VM
2. Copie o IP público
3. No terminal:
   ssh azureuser@<ip-publico>

## Etapa 4: Teste de Conectividade

1. Dentro da VM:
   sudo apt update

   Se funcionar, a VM está com acesso à internet.