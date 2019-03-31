Ustawianie parametrów sieci
---------------------------

![alt text][network]

[network]: ./network.png "Logo Title Text 2"

1. na 1 z komputerów zainstaluj oprogramowanie ``http-chat`` dostępne pod adresem ``https://github.com/jkanclerz/http-chat``

Wejściowe parametry sieci
-------------------------
| Parametr | wartość | komentarz(opcionalny) |
| ------------- |:-------------:| -----:|
|   PC 1 | debian 9.8 |
| IP - address  | 10.0.2.15 | |
| MASKA  | 	/24 | |
|   |  | |
| PC 2  | debian 9.8 | |
| IP - address  | 192.168.10.5 | |
| MASKA  | /24| |

Weryfikacja połączenia

Polecenie
ping <adres ip>

Efekt
64 bytes from 172.16.100.11 icmp_seq=1 ttl=64 time=0.637 ms

Statyczna konfiguracja parametrów połączenia
Aby konfiguracja sieci na wirtualnych maszynach była zapisana po ich restarcie należy w zapisać w pliku lokalizacji : /etc/network/interrfaces np. |``Iface enp0s3 inet static Adress 192.168.100.1 Netmask 255.255.255.0

Auto enp0s8 Iface enp0s8 inet static Adress 192.168.200.1 Netmask 255.255.255.0 Up ip route add 192.168.0.0/24 via 192.168.200.2 Down ip route del 192.168.0.0/24``|

Wejściowe parametry sieci
-------------------------
| Parametr | wartość | komentarz(opcionalny) |
| ------------- |:-------------:| -----:|
|   PC 1 |  
| IP - address  | 192.168.10.10 | |
| MASKA  | 255.255.255.0 | |
|   |  | |
| PC 2  |  | |
| IP - address  | 172.16.100.100 | |
| MASKA  | 255.255.0.0 | |

Weryfikacja połączenia

Polecenie

ping
```
ping
```
Efekt
```
```

Nowa statyczna konfiguracja 

-------------------------
| Parametr | wartość | komentarz(opcionalny) |
| ------------- |:-------------:| -----:|
|   PC 1 |  
| IP - address  |  | |
| MASKA  |  | |
|   |  | |
| PC 2  |  | |
| IP - address  |  | |
| MASKA  |  | |

Weryfikacja połączenia

Polecenie
```
```

Efekt
```
```

Warto wiedzieć
--------------

-------------------------
| Parametr | wartość | komentarz(opcionalny) |
| ------------- |:-------------:| -----:|
| Lokalizacja pliku z konfiguracją sieci| /sbin | |
| UP -> Wyłączenie interfejsu sieciowego| ifup | |
| DOWN -> Włączenie interfejsu sieciowego| ifdown | |
| Sprawdzenie obecnych parametrów | ip a | |
| lista wszystkich interfejsów | ip addr | |
| Które interfejsy jakie porty słuchają | | |

