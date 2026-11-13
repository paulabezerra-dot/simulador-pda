# Simulador PDA — Processamento

## O que está incluído
- Aplicação web responsiva para celular e computador.
- Leitura de QR Code pela câmera usando html5-qrcode.
- Modo de teste por digitação de código.
- Base local de TOs e pacotes, com importação CSV.
- Validação de destino, duplicidade, pacotes de tratativa e códigos não cadastrados.
- Sons simples de sucesso e erro.
- Resumo de atividade e exportação do histórico CSV.
- Estrutura PWA para instalação pela opção "Adicionar à tela inicial".

## Como testar no computador
Abra `index.html` em um navegador. A câmera pode não funcionar em `file://`; para testar câmera, hospede em HTTPS.

## Como publicar gratuitamente
1. Crie uma conta em GitHub.
2. Crie um repositório público chamado `simulador-pda`.
3. Envie os arquivos desta pasta para a raiz do repositório.
4. Em Settings > Pages, escolha Deploy from a branch, selecione `main` e `/root`.
5. Aguarde o endereço HTTPS ser publicado.
6. Abra o endereço no celular e autorize a câmera.
7. Android: menu do Chrome > Instalar app/Adicionar à tela inicial.
   iPhone: Safari > Compartilhar > Adicionar à Tela de Início.

## Base CSV
Cabeçalho: `tipo,codigo,destino`
- `TO,TO12345,SP2`
- `PACOTE,PKG0001,SP2`
- `TRATATIVA,PKG0002,TRATATIVA`

O QR Code da TO deve conter somente o código cadastrado (ex.: `TO12345`).
O QR Code do pacote deve conter somente o código cadastrado (ex.: `PKG0001`).
O destino é consultado na base do aplicativo.

## Importante
Esta é uma primeira versão de protótipo. Não se conecta ao PDA ou aos sistemas da Shopee. A biblioteca de leitura de QR é carregada de uma CDN, então a primeira abertura do leitor exige internet. A leitura pela câmera requer HTTPS e permissão do usuário. O suporte nativo a PWA e câmera pode variar entre navegadores.
