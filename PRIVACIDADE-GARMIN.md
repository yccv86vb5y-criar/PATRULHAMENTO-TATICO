# Política de privacidade — Patrulhamento Tático para Garmin

Atualização: 27 de outubro de 2026. Aplicável à versão beta 0.1.0 para o Garmin Forerunner 265, identificador 219782d26e1b4b18b549e324c93cc526.

Esta página descreve o aplicativo do relógio. Não descreve o site de mapas que também usa o nome Patrulhamento Tático.

## Responsável e contato

O aplicativo é mantido pelo desenvolvedor identificado pela conta GitHub [yccv86vb5y-criar](https://github.com/yccv86vb5y-criar). Dúvidas e solicitações sobre o aplicativo podem ser encaminhadas pelo recurso **Contatar desenvolvedor** da sua página no Connect IQ. Para questões sobre informações tratadas pela Garmin ou Geoapify, consulte também os canais dos respectivos provedores indicados abaixo.

## Localização e finalidade

Ao abrir o aplicativo e iniciar o monitoramento pelo botão START, o código utiliza a posição obtida pelo GPS do relógio para identificar a área de policiamento e a delegacia cadastradas. O aplicativo mantém em memória posições recentes, a última área e os resultados necessários para confirmar mudanças e emitir alertas por vibração.

O reconhecimento de áreas e delegacias é realizado no relógio, usando os limites incluídos no aplicativo. Essas verificações locais não enviam a posição ao desenvolvedor.

## Consulta opcional de nomes de ruas

A função de ruas só faz consultas externas se o usuário configurar uma chave da API Geoapify nas configurações do aplicativo e iniciar o monitoramento. A versão distribuída começa com essa chave vazia.

Quando habilitada e com conexão disponível, o aplicativo envia **latitude, longitude, chave da API e parâmetros da consulta**, como idioma e tipo de resultado, para `https://api.geoapify.com/v1/geocode/reverse`, por HTTPS, utilizando a conexão disponibilizada pelo Garmin Connect e pelo celular emparelhado. O objetivo é obter o nome da rua e identificar mudanças. A chave é usada para autenticar e contabilizar o uso da conta do usuário no provedor.

Não há servidor próprio do desenvolvedor recebendo essas consultas na versão 0.1.0. Entretanto, Garmin e Geoapify tratam as informações necessárias ao funcionamento dos seus serviços segundo suas próprias políticas.

A Geoapify informa que registra informações técnicas das requisições, inclusive dados da requisição, cabeçalhos, endereço IP e horário, para controle de acesso, contabilização e operação do serviço. O tratamento e os prazos desse provedor são descritos na [política de privacidade da Geoapify](https://www.geoapify.com/privacy-policy/). O desenvolvedor do aplicativo não controla esses registros.

Veja também as [informações de privacidade da Garmin](https://www.garmin.com/privacy/).

## Armazenamento e outros dados

O código do aplicativo não cria histórico persistente de percursos ou posições, não grava atividades de patrulhamento e não possui banco de dados de deslocamentos do desenvolvedor. As posições e resultados recentes necessários ao funcionamento permanecem na memória da sessão; deixar de monitorar não cria um arquivo de percurso.

A chave da API é uma configuração persistente administrada pela plataforma Garmin. Ela não é incluída nos arquivos públicos do projeto nem enviada a um servidor do desenvolvedor pelo código do app. Proteja a chave e não a publique em repositórios ou mensagens.

O código não acessa contatos, mensagens, microfone, frequência cardíaca ou dados de pagamento e não inclui publicidade nem ferramentas de análise de uso. O tratamento realizado pela plataforma Garmin e pelos serviços externos é regido também pelas políticas desses provedores.

## Controle pelo usuário

- Pressionar START novamente pausa o monitoramento e impede novas consultas pelo aplicativo. Consultas já enviadas podem ter sido processadas pelo provedor.
- Sair do aplicativo encerra o monitoramento GPS iniciado por ele.
- Para desativar as consultas de ruas, apague a chave Geoapify nas configurações e reinicie o aplicativo. As verificações locais de áreas continuam disponíveis.
- Desinstalar o aplicativo remove seu uso do relógio. Isso não apaga automaticamente registros mantidos pela Garmin ou Geoapify.
- Para solicitações relativas a dados mantidos por esses serviços, utilize os canais de privacidade dos respectivos provedores.

## Alterações

Esta política deverá ser atualizada se o aplicativo passar a usar outros serviços ou a armazenar ou compartilhar outros dados. Consulte esta página ao instalar uma nova versão.
