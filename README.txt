-Il framework prevede la presenza di un server e di un client.
-Il client ha inizia l'inferenza sulla sua parte di rete neurale (MobileNet in questo caso) prende Il risultato intermedio ottenuto e lo inoltra al 
 server via socket. IL server, accetta la connesione e completa l'inferenza.
-Il framework prevede l'inoltro del risultato dell'inferenza dal server al client
 in quanto si suppone che sia lui lo user del servizio di inferenza.
-la comunicazione di default avviene su localhost:8078
-la cartella contiene notebook ipynb. Per eseguirli direttamente da riga di comando
 è necessario convertirli in script .py con il seguente comando da lanciare su jupyter: 
           
           1)  pip install ipynb-py-convert
           2)  ipynb-py-convert Ex/abc.ipynb Ex/abc.py

