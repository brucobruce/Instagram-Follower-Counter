Questo codice utilizza un'API di Instagram per acquisire il numero di follower di un utente specifico, quindi invia i dati a un broker MQTT che li trasmette a un chip ESP-32.

è necessario importare i moduli con i seguenti comandi:

const express = require('express');
const path = require('path');
const https = require('https');
const mqttClient = require('./mqtt');

per poi creare un express application usando const app = express(); per poi mandarlo a una directory publica con questa funzione : app.use(express.static(path.join(__dirname, 'public')));
Dobbiamo dare un'identità al nostro follower counter , si chiamerà "iismarconicivitavecchia" , per assegnargli un nome usiamo questa funzione : const username = "iismarconicivitavecchia";
