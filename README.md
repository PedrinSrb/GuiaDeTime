# Guia de Times — Versão com Permissão Android ⚽📍

## Descrição

O Guia de Times é um aplicativo Android desenvolvido em Kotlin que permite consultar informações sobre clubes de futebol e ligas esportivas utilizando a API-Football.

Nesta nova versão, o aplicativo foi evoluído para utilizar a localização do usuário, permitindo identificar automaticamente o país atual e exibir as principais ligas de futebol disponíveis naquela região.

---

## Relação com a atividade anterior

Na atividade anterior, o aplicativo permitia pesquisar times e ligas manualmente através do nome informado pelo usuário.

Nesta versão foi adicionada uma nova funcionalidade chamada **"Ligas do Meu País"**, que utiliza a localização atual do dispositivo para descobrir o país do usuário e consultar automaticamente as ligas disponíveis através da API-Football.

---

## API utilizada

* Nome da API: API-Football (API Sports)

### Endpoints utilizados

* `/teams?search={nome}`
* `/leagues?search={nome}`
* `/leagues?country={pais}`
* `/standings?league={id}&season={ano}`

### Dados exibidos no aplicativo

#### Times

* Nome
* País
* Fundação
* Estádio
* Capacidade
* Escudo

#### Ligas

* Nome da liga
* País
* Tipo
* Logo da competição
* Classificação da liga

#### Localização

* País detectado
* Lista de ligas do país atual

---
O aplicativo utiliza a permissão INTERNET para realizar requisições à API pública.

```xml
<uses-permission android:name="android.permission.INTERNET" />
```
## Permissão Android utilizada

### Permissão escolhida

```xml
<uses-permission android:name="android.permission.ACCESS_FINE_LOCATION" />
<uses-permission android:name="android.permission.ACCESS_COARSE_LOCATION" />
```

### Onde foi declarada

Arquivo:

```text
AndroidManifest.xml
```

### Por que essa permissão é necessária

A localização é utilizada para identificar automaticamente o país onde o usuário está e buscar as ligas de futebol correspondentes através da API-Football.

### Quando a permissão é solicitada

A permissão é solicitada somente quando o usuário pressiona o botão:

```text
📍 LIGAS DO MEU PAÍS
```

---

## Fluxo da permissão

### 1. Permissão já concedida

O aplicativo obtém a localização atual do usuário e consulta as ligas do país identificado.

### 2. Usuário concede a permissão

O aplicativo acessa a localização do dispositivo, identifica o país e exibe as ligas encontradas.

### 3. Usuário nega a permissão

O aplicativo exibe uma mensagem explicando que a localização é necessária para utilizar a funcionalidade e continua funcionando normalmente para pesquisas de times e ligas.

---

## Funcionalidades

* Consumo de API pública
* Pesquisa de times por nome
* Pesquisa de ligas por nome
* Consulta automática de ligas por localização
* Validação de entrada
* Tratamento de campo vazio
* Exibição de informações detalhadas
* Exibição de logos e escudos
* Tratamento de falhas de conexão
* Tratamento de permissão concedida
* Tratamento de permissão negada
* Feedback ao usuário durante as consultas

---

## Tecnologias utilizadas

* Kotlin
* Android Studio
* XML
* Retrofit
* Gson Converter
* OkHttp
* Glide
* Google Play Services Location
* API-Football
* Permissão ACCESS_FINE_LOCATION

---

## Como executar o projeto

1. Baixar o arquivo zip.
2. Extrair o arquivo.
3. Abrir o projeto no Android Studio.
4. Aguardar a sincronização do Gradle.
5. Executar o aplicativo em um emulador ou dispositivo Android.
6. Testar a pesquisa de times e ligas.
7. Testar o botão **📍 LIGAS DO MEU PAÍS**.
8. Conceder ou negar a permissão para verificar o comportamento do aplicativo.

---

## Prints do aplicativo

### Tela Inicial

  <img width="393" height="852" alt="Screenshot_62" src="https://github.com/user-attachments/assets/4e4151ba-2353-47c6-bdd0-05711bc1215f" />

### Consulta de Time

  <img width="391" height="847" alt="Screenshot_63" src="https://github.com/user-attachments/assets/12da175a-f68b-4b98-b996-d77cd508910a" />

### Consulta de Liga

   <img width="376" height="862" alt="Screenshot_64" src="https://github.com/user-attachments/assets/738e5e00-48e5-443e-bc3d-1d0d0d7d5592" />

### Solicitação de Permissão

  
  <img width="314" height="678" alt="Screenshot_91" src="https://github.com/user-attachments/assets/eaa7298f-76f8-42f1-8b71-7dd8678dd275" />


### Resultado da Localização

  
  <img width="314" height="671" alt="Screenshot_92" src="https://github.com/user-attachments/assets/816307d5-e63d-47e0-829e-c4abdb9e8d57" />


---

## Autor

Pedro Henrique De Oliveira Cadiz
