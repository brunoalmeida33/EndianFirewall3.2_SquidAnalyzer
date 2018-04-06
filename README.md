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

Realizando Download:

    curl -Lo squidanalyzer-endian3-1.0-1.x86_64.rpm  https://github.com/brunoalmeida33/EndianFirewall3.2_SquidAnalyzer/raw/master/squidanalyzer-endian3-1.0-1.x86_64.rpm
    
<br>
    
Executando a instalação:

    rpm -Uvh squidanalyzer-endian3-1.0-1.x86_64.rpm
    
   <br>

Configuração de adicional (Recomendado):

<br>

Com qualquer editor (vim ou nano), edite o arquivo do logrotate do squid abaixo.

<br>

nano /etc/logrotate.d/squid.tmpl

<br>

Substitua a linha abaixo:

<br>

/var/log/squid/access.log_short {
    daily
    # rotate 1 is necessary for squid-graph in order to create
    # a 24h graph.
    rotate 1  #EDITAR ESSA LINHA
    nocompress
    missingok
    sharedscripts
    lastaction
    /etc/init.d/syslog-ng reload
    endscript
}

<br>

Editar Para:

<br>

/var/log/squid/access.log_short {
    daily
    # rotate 1 is necessary for squid-graph in order to create
    # a 24h graph.
    rotate 94    #VALOR RECOMENDADO
    nocompress
    missingok
    sharedscripts
    lastaction
    /etc/init.d/syslog-ng reload
    endscript
}

<br>

Salve e feche o arquivo, apos reinicie o Servidor Firewall.

<br>
<\p>

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
  
  
