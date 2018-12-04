
Network address: 	 11000000 10100000 00000000 00000000	192.160.0.0 INTERFACE
Netmask:          	 11111111 11110000 00000000 00000000	255.240.0.0 (12 bits)  = Se é 12 bits, a mascara após 12 bits pode colocar tudo em 1.
Broadcast addr:   	 11000000 10101111 11111111 11111111	192.175.255.255 
Min Host value:   	 11000000 10100000 00000000 00000001	192.160.0.1 
Max Host value:   	 11000000 10101111 11111111 11111110

----------BROADCAST
Um endereço de broadcast [1] é um endereço que permite que as informações sejam enviadas para todas as interfaces em uma determinada sub-rede,
 em vez de uma máquina específica. Geralmente, o endereço de broadcast é encontrado obtendo-se o complemento de bit da máscara de sub-rede e
 executando uma operação OR bit a bit com o identificador de rede. Em outras palavras, o endereço de broadcast é o último endereço no
 intervalo de endereços da sub-rede. Por exemplo, o endereço de broadcast da rede 192.168.5.0 é 192.168.5.255. Para redes de tamanho / 24 ou maior,
 o endereço de broadcast sempre termina em 255.


----------DNS

Resolução de endereço 
Artigo principal: Sistema de Nomes de Domínio
Os hosts na Internet geralmente são conhecidos por nomes, por exemplo, www.example.com, não principalmente por seu endereço IP,
 que é usado para roteamento e identificação de interface de rede. O uso de nomes de domínio requer a tradução, chamada resolvê- los para endereços
 e vice-versa. Isso é análogo a procurar um número de telefone em um catálogo telefônico usando o nome do destinatário.

A tradução entre endereços e nomes de domínio é realizada pelo Sistema de Nomes de Domínio (DNS), um sistema de nomes distribuído hierárquico que permite
 a subdelegação de espaços de nomes para outros servidores DNS.



--------------------EXPLICAÇÕES SOBRE COMUNICAÇÕES DE REDE-CURSO ALURA------------------

--DNS- traduz url para o endereço ip
--Apresentação/ Presentation - Camada de apresentação e estilos
--Sessão/Session - Abre uma sessão, separando de outras abas e outros conteúdos.
--Transporte/Transport - Verificar de como o transporte vai ser feito :

TCP: Transporte seguro, verificar se tudo que está sendo enviado, está sendo recebido.
UDP: Transporte não seguro, não verifica se está sendo recebido corretamente.

Quando faço uma requisição em uma página web pelo http/get, está implícito uma porta de Destino, no caso da http seria a porta 80
e uma porta de origem, que o meu sistema operacional disponibiliza.
Exemplo?  Proto          Endereço Local                 Endereço Externo             Estado
	   TCP       192.168.121.171:52352              bn3sch020010637:https     ESTABILISHED             : Isso se chama de segmento
           TCP       192.168.121.171:42652              gr3sch020010637:https     TIME_WAIT                : Isso se chama de segmento

No endereço local, a parte depois dos dois pontos, é a porta que o sistema disponibilizou.

--Rede/Network - Essa camada encapsula todo o seguimento da camada de transporte, seguido do ip de destino e do ip de origem.                   Packages:Pacotes
--Data-link    - Essa camada encapsula todo o seguimento da camada de transporte, seguido do ip de destino e do ip de origem e seguidas do endereço mac de destino e de origem.         Frames
Agora só falta passar a informação, agora passamos a responsabilidade para a camada física, que são os cabos e a informação é passada por meio de sinais elétricos.
--Physical - Empresas e roteadores : Mandadá todos os dados anteriores para o servidor, fazendo uma requisição.



 -------------------Servidor----------------
Physical - Recebemos os dados na camada física, estes emcapsulados, que será http/get/da/sa/da/sa/da/sa anteriormente.

Data-Link - Recebe a informação dos cabos(Physical) e ela vai interpretar o endereçamento mac e verá qual site o cliente quer acessar.

Network - Essa camada vai verificar os endereços ips, e verá que o endereço ip de destino é de fato o conteúdo do blog do site.
Transport - Vai ver as portas de comunicação que queremos acessar.
Sessio - 
Presentation

Aplication - Chega a requisição http/get no servidor, uma vez que ele recebe essa requisição, ele precisa mandar de volta a informação para o cliente
 e assim, passará pelas camadas tudim de novo, só que o inverso, os endereços de destino será o cliente, e o de origem o servidor.
