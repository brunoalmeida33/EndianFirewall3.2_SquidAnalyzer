# EndianFirewall3.2_SquidAnalyzer
 Addon SquidAnalyzer report for Endian Firewall Community 3.2.x.


Versão:
--------

v.1.0 ( Testado no Endian Firewall Community nas versões 3.2.1 a 3.2.5).



Requerimentos/opcional:
--------
- Requer: Acesso ao seu Endian Firewall atraves do console (Conexão SSH).



Instalando o Pacote:
--------

Realizando Download:

    curl -Lo squidanalyzer-endian3-1.0-1.x86_64.rpm 
    
    
Executando a instalação:

    rpm -Uvh squidanalyzer-endian3-1.0-1.x86_64.rpm
    

Removendo o pacote:
--------
- No console ssh digite:

    rpm -e squidanalyzer-endian3
    
    
    
Outras informações:
------------------

- Para acessar o SquidAnalyzer é necessario acessar o Servidor firewall com login padrão "admin" e sua senha atual.

Link Para acesso: HTTPS://IPDOFIREWALL:10443/squidanalyzer/

Observações: Os relatorios são atualizados a cada hora automaticamente, inicialmente nenhum relatorio é gerado, caso queira executa-lo manualmente, é necessario logar no SSH como root e executar o comando "squid-analyzer". 

Espero ter ajudado.

Atenciosamente,

Bruno Almeida.
  
  
