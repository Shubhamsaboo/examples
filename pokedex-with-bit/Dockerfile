FROM jinaai/jina:1.0.5

# setup the workspace
COPY . /workspace
WORKDIR /workspace

RUN apt-get update && apt-get install --no-install-recommends -y git curl libmagic1 wget tar \
    && pip uninstall -y jina && pip install -r requirements.txt

RUN bash get_data.sh && bash download.sh && python app.py index

ENTRYPOINT ["python", "app.py", "search"]

LABEL author="Jina AI Dev-Team (dev-team@jina.ai)"
LABEL type="app"
LABEL kind="example"
LABEL avatar="None"
LABEL description="Jina App to search Pokemons using Google Big Transfer Model as Encoder"
LABEL documentation="https://github.com/jina-ai/examples/tree/master/pokedex-with-bit"
LABEL keywords="[pokemon, cv, Google Big Transfe]"
LABEL license="apache-2.0"
LABEL name="pokedexwithbit"
LABEL platform="linux/amd64"
LABEL update="None"
LABEL url="https://github.com/jina-ai/examples/tree/master/pokedex-with-bit"
LABEL vendor="Jina AI Limited"
LABEL version="0.0.1"
