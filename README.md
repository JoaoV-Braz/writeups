# writeups
Análises e relatórios técnicos de segurança

Durante uma verificação de segurança, identifiquei a porta TCP 631 aberta, associada ao CUPS 2.4, serviço de impressão do Linux.

Executei `nmap -sV localhost` para identificar os serviços ativos. Após investigar os riscos, restringi o acesso externo à porta, mantendo o serviço disponível localmente.

A medida reduziu a exposição do CUPS à rede, preservando seu funcionamento local. O caso reforçou a importância de verificar serviços habilitados por padrão e limitar o acesso aos estritamente necessários, além de manter o software atualizado para corrigir possíveis vulnerabilidades.

Para validar a configuração, é necessário testar a porta a partir de outro dispositivo da rede e verificar se o CUPS está escutando apenas em localhost. Assim, é possível confirmar se a restrição foi aplicada corretamente e se o serviço continua funcionando conforme esperado.
