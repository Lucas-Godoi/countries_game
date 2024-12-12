# Projeto REST Client: Busca e Jogos sobre Países

Este projeto implementa três funcionalidades principais:

1. **Busca de informações por países:** pesquisa dados de um país utilizando a API REST do [Rest Countries](https://restcountries.com) e exibe um mapa interativo com as informações.
2. **Jogo de adivinhação de bandeiras:** apresenta uma bandeira através da API REST do [Rest Countries](https://restcountries.com) e desafia o usuário a identificar o país correspondente.
3. **Jogo de adivinhação de capitais:** apresenta o nome de uma capital através da API REST do [Rest Countries](https://restcountries.com) e desafia o usuário a identificar o país correspondente.

## Tecnologias utilizadas
- **Python**
- **Jupyter Notebook**
- **Bibliotecas**:
  - `requests`
  - `folium`
  - `ipywidgets`

## Instalação

1. Certifique-se de ter o Python (versão 3.8 ou superior) instalado.
2. Crie e ative um ambiente virtual:

   ```bash
   python -m venv venv
   source venv/bin/activate # Para Linux/Mac
   venv\Scripts\activate   # Para Windows
   ```

3. Instale as dependências necessárias:

   ```bash
   pip install requests folium ipywidgets
   ```

4. Instale o Jupyter Notebook:

   ```bash
   pip install notebook
   ```

5. Inicie o Jupyter Notebook:

   ```bash
   jupyter notebook
   ```

6. Abra o arquivo `countriesAPI.ipynb` e execute as células sequencialmente.

## Documentação da API REST

O projeto utiliza a API do [Rest Countries](https://restcountries.com), que fornece informações sobre países em formato JSON.

### Endpoints utilizados

#### Busca de dados de um país
- **URL:** `https://restcountries.com/v3.1/name/{country}?fields=name,latlng,flags,region,subregion,population,capital,demonyms`
- **Método:** `GET`
- **Autenticação:** Não requer autenticação.
- **Exemplo de resposta:**

  ```json
  [
    {
      "name": {
        "common": "Brazil"
      },
      "latlng": [-14.235, -51.9253],
      "flags": {
        "png": "https://flagcdn.com/w320/br.png"
      },
      "region": "Americas",
      "subregion": "South America",
      "population": 212559417,
      "capital": ["Brasília"],
      "demonyms": {
        "eng": {
          "m": "Brazilian",
          "f": "Brazilian"
        }
      }
    }
  ]
  ```

#### Busca de todos os países
- **URL:** `https://restcountries.com/v3.1/all?fields=name,flags,capital,region`
- **Método:** `GET`
- **Autenticação:** Não requer autenticação.
- **Exemplo de resposta:**

  ```json
  [
    {
      "name": {
        "common": "Brazil"
      },
      "flags": {
        "png": "https://flagcdn.com/w320/br.png"
      },
      "capital": ["Brasília"],
      "region": "Americas"
    },
    ...
  ]
  ```

## Funcionalidades do Projeto

### 1. Busca de países no mapa
![image](https://github.com/user-attachments/assets/b6744495-e7e9-4a8b-ba87-f64156b29404)


Ao inserir o nome de um país, o programa utiliza a API para buscar informações como:
- Nome
- Localização (latitude e longitude)
- Bandeira
- Região/Sub-região
- População
- Capital

As informações são exibidas em um mapa interativo com marcadores.

#### Execução
1. Insira o nome do país no campo de busca.
2. Clique no botão "Search".
3. O mapa interativo será exibido com as informações detalhadas.

### 2. Jogo de adivinhação de bandeiras
![image](https://github.com/user-attachments/assets/54858b2b-452f-4c53-97c9-647f47402b3f)

- O programa exibe uma bandeira que foi requisitada através da API REST.
- O usuário deve selecionar o nome do país correspondente entre as opções apresentadas.
- A cada rodada, a pontuação é atualizada, e o jogo dura 5 rodadas.

#### Execução
1. Execute a célula que inicia o jogo.
2. Observe a bandeira apresentada.
3. Escolha o país correto entre as opções.
4. Avance para a próxima rodada até o final do jogo.

### 3. Jogo de adivinhação de capitais
![image](https://github.com/user-attachments/assets/0f82a4dd-79c1-46f2-abc3-78cb03d2ec31)

- O programa exibe o nome de uma capital que foi requisitada através da API REST.
- O usuário deve selecionar o país correspondente entre as opções apresentadas.
- Assim como no jogo de bandeiras, o jogo possui 5 rodadas e atualiza a pontuação a cada resposta.

#### Execução
1. Execute a célula que inicia o jogo.
2. Observe o nome da capital apresentado.
3. Escolha o país correto entre as opções.
4. Avance para a próxima rodada até o final do jogo.

## Teste operacional

1. Execute o arquivo `countriesAPI.ipynb` em um ambiente Jupyter Notebook.
2. Teste as três funcionalidades:
   - Pesquise por países e visualize o mapa interativo.
   - Participe do jogo de adivinhar o país através da bandeira.
   - Participe do jogo de adivinhar o país através da capital.
  
   

