# writeups
Análises e relatórios técnicos de segurança
-------------------------------------------------
Durante uma verificação de segurança, identifiquei a porta TCP 631 aberta, associada ao CUPS 2.4, serviço de impressão do Linux.

Executei `nmap -sV localhost` para identificar os serviços ativos. Após investigar os riscos, restringi o acesso externo à porta, mantendo o serviço disponível localmente.

<img width="513" height="120" alt="image" src="https://github.com/user-attachments/assets/ee3132e9-83b8-4474-8120-a56f71e4f2c7" />

A medida reduziu a exposição do CUPS à rede, preservando seu funcionamento local. O caso reforçou a importância de verificar serviços habilitados por padrão e limitar o acesso aos estritamente necessários, além de manter o software atualizado para corrigir possíveis vulnerabilidades.

<img width="485" height="227" alt="image" src="https://github.com/user-attachments/assets/c94d38bc-dbe9-4dbc-9796-36d1f84396f8" />

Para validar a configuração, é necessário testar a porta a partir de outro dispositivo da rede e verificar se o CUPS está escutando apenas em localhost. Assim, é possível confirmar se a restrição foi aplicada corretamente e se o serviço continua funcionando conforme esperado.

<img width="810" height="258" alt="image" src="https://github.com/user-attachments/assets/4fcbe247-bfce-4b70-b9cd-2f0c00b50eb5" />
