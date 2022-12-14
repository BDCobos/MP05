# Activitats: 

Per dibuixar els diagrames de flux podeu fer servir [draw.io](https://draw.io) o qualsevol altra eina online.

**1. Calcula el CC de les següents figures:**

**Fórmula --> CC = núm de branques - núm de nodes + 2**

  - ![image](https://user-images.githubusercontent.com/110727546/204613022-4ab64342-2e06-438d-a7e8-570685b3c406.png)

**Resultat 1:**

CC = 16 - 14 + 2 = 4 

  - ![image](https://user-images.githubusercontent.com/110727546/204613180-6d55bf09-28b8-417e-96f4-f71a762ac44c.png)

**Resultat 2:**

CC = 16 - 14 + 2 = 4 

  - ![image](https://user-images.githubusercontent.com/110727546/204655229-8c3f28d7-3d8b-4746-a55d-331f89da39d2.png)

**Resultat 3:**

CC = 8 - 6 + 2 = 4 

**2. Dibuixa el diagrama de flux representat per aquest codi i després calcula la seva CC:**

  - ![image](https://user-images.githubusercontent.com/110727546/204615125-363e5e6c-173b-4ec0-8c0b-cb97985ade06.png)

  - **Diagrama:**

![image](https://user-images.githubusercontent.com/113586156/204752071-57905cb1-101a-4d00-9e1d-ad248651dceb.png)

  - **Resultat CC:**

**Fórmula --> núm de sentències + 1** 

CC = 1 + 1 = 2 

**3. Dibuixa el diagrama de flux representat per aquest codi i després calcula la seva CC:**

```
public class proves {
    public static  String queEmPoso(int temperatura) {
        String roba = "res";
        if(temperatura<0){
           roba = "roba d'esquiar";
        }
        else if(temperatura<10){
           roba = "roba de muntanya";
        }
        else if(temperatura<20){
           roba = "roba d'hivern";
        }
        else if(temperatura<30){
           roba = "roba d'estiu";
        }
        return roba;
    }    
}
```

  - **Diagrama:**

![image](https://user-images.githubusercontent.com/113586156/204762599-f887fafe-5023-4d61-ac90-e936e737fe36.png)

  - **Resultat CC:**

CC = 4 + 1 = 5 

  - **Resultat proves camins:**

Prova 1 --> int res = -2 -- res < 0 -- output = roba d'esquiar

Prova 2 --> int res = 5  -- res < 10 -- output = roba de muntanya 

Prova 3 --> int res = 12 -- res < 20 -- output = roba d'hivern

Prova 4 --> int res = 25 -- res < 30 -- output = roba d'estiu

Prova 5 --> int res = 35 -- res > 30 -- output = roba

**4. Dibuixa el diagrama de flux representat per aquest codi, calcula la seva CC i crea una prova per a cada camí posible:**

```
    public static Boolean llumsEncesos(int hora) {
        Boolean llums = false;
        if(hora <= 8 || hora >= 20){
            llums = true;
        }
        return llums;
    }
```
  - **Diagrama:**

![image](https://user-images.githubusercontent.com/113586156/204760619-9cfac567-5545-49ba-bfac-8fd6715505c3.png)

  - **Resultat CC:**

CC = 1 + 1 = 2

  - **Resultat proves camins:**

Prova 1 --> int hora = 12 -- hora <= 8 || hora >= 20 -- output = false (apagada)

Prova 2 --> int hora = 6 -- hora <= 8 || hora >= 20 -- output = true (encesa)

**5. Investiga sobre les proves de caixa negra:**

  - Què són?

Són un tipus de proves de programari que es basen en la creació dels casos de proves analitzant l'especificació del component, ignorant el funcionament intern del sistema o component, centrant-se en les sortides generades basant-se en unes entrades i condicions d'execució concretes.

![image](https://user-images.githubusercontent.com/113586156/204763955-93ffe7be-2170-4b1c-8e42-1a9929de444f.png)

  - Quina diferència principal tenen sobre les de caixa blanca?

La diferència principal entre caixa blanca i negra, es què per realitzar una prova de caixa blanca necessitem conèixer el codi que estem testejant i per realitzar una prova de caixa negra ignora el funcionament intern del sistema o component.
