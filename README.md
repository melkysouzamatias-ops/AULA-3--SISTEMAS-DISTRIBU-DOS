# AULA-3--SISTEMAS-DISTRIBU-DOS

Aula 03: Comunicação Não Orientada à Conexão (UDP) com Sockets em Python
Seja bem-vindo ao repositório da terceira aula da disciplina de Sistemas Distribuídos!

Nesta aula, evoluímos a comunicação entre processos explorando o protocolo UDP (User Datagram Protocol). Ao contrário do TCP trabalhado na Aula 02, o UDP é um protocolo sem conexão e não orientado a fluxo, ideal para cenários onde velocidade e baixo overhead são mais prioritários do que a garantia de entrega de cada pacote.

📌 Conteúdos Abordados
1. Entendendo o Protocolo UDP
SOCK_DGRAM vs SOCK_STREAM: No módulo socket, o parâmetro socket.SOCK_DGRAM configura o uso de datagramas UDP em vez do fluxo TCP.

Ausência de Handshake: O cliente não precisa estabelecer uma conexão prévia com o servidor antes de enviar dados (não existem as chamadas listen() ou accept() no lado do servidor).

Datagramas Independentes: As mensagens são enviadas como pacotes individuais (datagrams) que contêm o endereço de destino diretamente no cabeçalho.

2. Destaques das Funções de Rede
recvfrom(buffer_size): Além dos dados recebidos, essa função retorna uma tupla (IP, Porta) identificando quem enviou o pacote.

sendto(bytes, (IP, Porta)): Envia o pacote de dados diretamente ao endereço especificado, sem requerer uma sessão aberta.
