# ITA
Projekt E-Vinjeta


## Veje:

V tej veji "microservices" bodo 3 storitve:

![image](https://user-images.githubusercontent.com/67262025/158026838-13eb06aa-1255-47de-8858-eaf4d2d1ed76.png)



Vsaka storitev ima 3 funkcionalne in 3 ne fukncionalne zahteve:


## REST API za zakup parkinega mesta:

![image](https://user-images.githubusercontent.com/67262025/158027025-57be1cb7-2b19-4686-a130-83ece654bd08.png)

Funkcionalne:
- Vpisovanje podatkov
- Izbira parkirnega mesta
- Status izvedbe akcije

Ne funkcionalne:

- Validacija podatkov v majn kot 10s
- Izbira parkirnega mesta
- Akcija se izvede v majn kot 30s

## gRPC storitev za uporabnike:

![image](https://user-images.githubusercontent.com/67262025/158068812-557d9724-cbbe-4502-b3d8-97ddfc2f3f87.png)

Funkcionalne:
- Obdelava zahteva za prijavo
- Seja uporanika
- Preverjanje registrkse številke

Ne funkcionalne:

- Da se pripravi povratni email v 30s
- Seja poteče v 1uri
- V primeru, da uporabnik ima že zakupljeno parkirno mesto se izpiše opozorilo

## REST API storitev za preverjanje parkiranega vozila:
![image](https://user-images.githubusercontent.com/67262025/158068789-c747d9fc-713b-475c-8b72-4b1b9322ebfc.png)


Funkcionalne:
- Preverjanje registrerske številke
- Priprava sporočila
- Pošiljanje sporočila

Ne funkcionalne:

- Preverjanje se izvede v 60s
- Priprava sporočila za opomin neobstajanje/neveljavnost registerske številke v 60s
- Sporočila se pošljejo v 60s

