# Struttura dei file

- inference_client.ipynb: client, esegue la prima parte della rete e invia il risultato al server
- inference_server.ipynb: server, riceve il risultato intermedio e completa l'inferenza
- LICENSE: licenza del progetto

# Flusso di lavoro

1. Il client carica un'immagine, la pre-processa e la passa attraverso la prima parte della rete neurale.
2. Il risultato intermedio viene serializzato e inviato al server tramite socket.
3. Il server riceve il dato, lo elabora con la seconda parte della rete e restituisce la predizione al client.
4. Il client riceve e visualizza il risultato finale.