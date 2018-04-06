# EndianFirewall3.2_SquidAnalyzer
 Addon SquidAnalyzer report for Endian Firewall Community 3.2.x.

<br>

Versão:
--------

v.1.0 ( Testado no Endian Firewall Community nas versões 3.2.1 a 3.2.5).

<br>

Requerimentos/opcional:
--------
- Requer: Acesso ao seu Endian Firewall atraves do console (Conexão SSH).

<br>

Instalando o Pacote:
--------

<br>

Realizando Download:

    curl -Lo squidanalyzer-endian3-1.0-1.x86_64.rpm  https://github.com/brunoalmeida33/EndianFirewall3.2_SquidAnalyzer/raw/master/squidanalyzer-endian3-1.0-1.x86_64.rpm
    
<br>

<br>

Executando a instalação:

    rpm -Uvh squidanalyzer-endian3-1.0-1.x86_64.rpm
    
<br>

Configuração Adicional (Recomendado para backups dos logs do squid):
--------
<br>

Edite o arquivo /etc/logrotate.d/squid.tmpl ( com qualquer editor de texto ) na linha 31, substitua o parametro "rotate 1" para "rotate 94", salve o arquivo e reinicie o servidor firewall.

Exemplo:

nano +31 /etc/logrotate.d/squid.tmpl 

Substitua "rotate 1" para "rotate 94" nesta linha. (obs: sem as aspas " " ).

Segure CTRL e pressione ENTER para salvar o arquivo e CTRL + x para sair do editor nano.

para reinicia o firewall utilize o comando "reboot".



Removendo o pacote:
--------
- No console ssh digite:

    rpm -e squidanalyzer-endian3
    
  <br>  
    
Outras informações:
------------------

- Para acessar o SquidAnalyzer é necessario acessar o Servidor firewall com login padrão "admin" e sua senha atual.

Link Para acesso: HTTPS://IPDOFIREWALL:10443/squidanalyzer/

Observações: Os relatorios são atualizados a cada 55 minutos automaticamente, inicialmente nenhum relatorio é gerado, caso queira executa-lo manualmente, é necessario logar no SSH como root e executar o comando "squid-analyzer". 

Espero ter ajudado.

Atenciosamente,

Bruno Almeida.
  
  
