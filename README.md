📝
# Redes-Hardware
Uma básica teoria sobre Redes e Hardware para começar nos estudos!

Resumos - Parte 1
Básico sobre Redes de Computadores

Começando pelas classes IP, elas foram criadas para definir a quantidade de endereços na rede como um todo. Atualmente em IPV4, existem 5 classes sendo elas:

Classe A -  Vai dos números 0 até 127
Classe B -  Vai dos números 128 até 191
Classe C -  Vai dos números 192 até 223
Classe D -  Vai dos números 224 até 239
Classe E -  Vai dos números 240 até 255

As numerações iniciais do endereço IP é que definem a classe a qual ele pertence, mas, nem todos os endereços podem ser utilizados. Existem alguns que são privados e restritos. Como por exemplo o 10.0.0.0, 172.16.0.0 e 192.168.0.0 são numeros privados, já os números 127.0.0.0 e 169.254.0.0 são números reservados, se você der um comando no sem prompt de comando da seguinte forma :

![Sem título](https://github.com/user-attachments/assets/febb2a70-fbd7-4d1c-8455-26f98808a0a3)

 
Como mostrado na imagem acima é uma forma de você analisar se sua placa de rede está com um bom funcionamento, pois quando você faz um ping com o ip 127, você está fazendo uma solicitação para sua própria placa de rede, caso não obtenha nenhuma resposta, pode ser um sinal de mal funcionamento da mesma. Já o IP 169.254.0.0 é o famoso APIPA, é considerado um erro quando ele aparecer, pois isso é um sinal que o fornecimento de endereço IP está com algum tipo de problema, se for o caso de DHCP por exemplo que fornece de forma automática, quando ele aparece esse endereço é um sinal que há algum problema de configuração no aparelho ou em alguma rota, pois ele não está conseguindo encontrar nada.
Um exemplo de uma rede tipo C seria da seguinte forma:

192.168.15.10 
Como podemos analisar no endereço IP acima, ele é de classe C. Sendo assim, ele é composto da seguinte forma, os três primeiros números 192.168.15 devem ser obedecidos em todos os endereços da rede, para que todos conectados nela consigam se comunicar. O número final é considerado o host, se tratando de um endereço de classe C essa rede suporta de 1 a 254, pois o endereço 192.168.15.0 é o endereço da rede e o 192.168.15.255 seria o endereço de broadcast dessa rede. 
As redes precisam de uma máscara para uma configuração total e funcionamento, elas são compostas em binário por 4 octetos, e também seguem o padrão de categoria de endereços, pois são as máscaras que vão determinar a quantidade de hosts naquele rede e a qual categoria o IP pertencerá. Você pode utilizar por exemplo uma máscara de rede de classe A em um IP 192.168.15.10 , porém toda a rede deverá seguir apenas o início do endereço que seria o 192, para que assim possam se conectar.
A máscara é constituída da seguinte forma:


255	.	255	.	255	.	255
A mesma máscara em binário:
11111111	.	11111111	.	.11111111	.	11111111
Como citado acima é composta por 4 octetos, que formam a máscara, ela possui o número 255 pois é o ultimo endereço possível em uma rede, e quando convertida para binário é representada por 11111111 por conta da soma da conversão. 

