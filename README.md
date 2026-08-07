# smiles-render-web

Online tool to help creating images from molecule SMILES.

## Running the API

### For Production with Docker Compose

#### Requirements

- `docker`
- `docker compose`

#### Running

``` bash
    docker compose up -d
```

`Docker Compose` will make sure to configure your `HTTP` and `HTTPS` connections and automatically map the respective `80` and `443` ports to the Smiles Render's `3000` application port.

### Local for development and tests

#### Requirements

- `mise`

#### Running

``` bash
    # Edit .env:
    cp .env.example .env
    vim .env

    # Install the correct python version and dependencies:
    mise install
    python3 -m venv .venv
    pip install -r requirements.txt

    # Running the API
    python3 src/main.py
```

now you can check if the API is running by performing a `GET` in [localhost:3000/ping](http://localhost:3000/ping) or simply running the web application accessing [http://localhost:3000](http://localhost:3000).
