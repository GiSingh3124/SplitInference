# SplitInference

Questo framework permette di eseguire l'inferenza di una rete neurale suddivisa tra client e server tramite socket.

## Struttura
- **inference_client.ipynb**: notebook che implementa il client. Esegue la prima parte della rete neurale (MobileNet), invia il risultato intermedio al server e riceve il risultato finale.
- **inference_server.ipynb**: notebook che implementa il server. Riceve il risultato intermedio dal client, completa l'inferenza e restituisce il risultato.
- **LICENSE**: licenza del progetto.

## Utilizzo
1. Convertire i notebook `.ipynb` in script `.py` se si desidera eseguirli da riga di comando:
   ```
   pip install ipynb-py-convert
   ipynb-py-convert SplitInference-main/inference_client.ipynb SplitInference-main/inference_client.py
   ipynb-py-convert SplitInference-main/inference_server.ipynb SplitInference-main/inference_server.py
   ```
2. Avviare prima il server, poi il client.
3. La comunicazione avviene su `localhost:8078`.

## Requisiti
- Python
- TensorFlow
- numpy
- pillow

## Note
Il client si occupa della prima parte dell'inferenza, il server la completa e restituisce il risultato al client.