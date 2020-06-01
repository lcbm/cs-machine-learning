# PCA e LDA: MNIST & LFW

Para esta atividade, escolha uma das seguintes bases:

- [`MNIST` (_Modified National Institute of Standards and Technology_)](http://yann.lecun.com/exdb/mnist/)
- [`LFW` (_Labeled Faces in the Wild_)](http://vis-www.cs.umass.edu/lfw/)

**Atividade 11**: Vamos utilizar imagens para entender como [`PCA` (_Principal Component Analysis_)](https://www.youtube.com/watch?v=FgakZw6K1QQ&feature=youtu.be) e [`LDA` (_Linear Discriminant Analysis_)](https://www.youtube.com/watch?v=azXCzI57Yfc&feature=youtu.be) podem ser utilizados como features em problemas de visão computacional.

**Instruções Gerais**:

1. Carregue uma das bases abaixo, diretamente do `sklearn`
   - MNIST (caracteres manuscritos)
     - `from sklearn.datasets import fetch_openml`
     - `X, y = fetch_openml('mnist_784', version=1, return_X_y=True)`
   - LFW (faces)
     - `from sklearn.datasets import fetch_lfw_people`
     - `faces = fetch_lfw_people(min_faces_per_person=60)`
2. [PCA (_Principal Component Analysis_)](https://www.youtube.com/watch?v=FgakZw6K1QQ&feature=youtu.be)
   - Aplique PCA avaliando o número de componentes necessários
   - Visualize as imagens associadas com os primeiros componentes: `pca.components_[i].reshape()`
   - Exiba a variância cumulativa
   - Compare as imagens de entrada com as imagens reconstruídas: `pca.transform` e `pca.inverse_transform`
3. [LDA (_Linear Discriminant Analysis_)](https://www.youtube.com/watch?v=azXCzI57Yfc&feature=youtu.be)
   - Aplique LDA nos dados originais
   - Exiba a projeção dos dados nos Discriminantes Lineares
   - Exiba a taxa de variância acumulada
4. Classificador
   - Aplique um classificador de sua escolha nas features obtidas por LDA e PCA
   - Compare os dois métodos e resultados

## 🐳 Docker installation and usage

### Requirements

- [Docker](https://docs.docker.com/get-docker/)
- [Docker-compose](https://docs.docker.com/compose/install/)

### Building and running

First, make sure you are inside this repository's directory:

```bash
cd <path/to/repo>
```

Then, start the container:

```bash
# start the container in the background of your terminal
docker-compose up --detach
```

At this point, the Jupyter Notebook will be running at `http://localhost:8888`.

### Installing new packages

There are a few ways you may install new packages to the container. It'll depend on your goal and needs.

#### Pip

If you need to do update or add packages via `pip`, execute the following command **inside your jupyter notebook**:

```bash
import sys

# install a pip package in the current Jupyter kernel
!{sys.executable} -m pip install <package>
```

> _**note**_: the `!` notation is used to run `pip` directly as a shell command from the notebook. Also, take a look [here](https://jakevdp.github.io/blog/2017/12/05/installing-python-packages-from-jupyter/) to see why you should NOT use `!pip install <package>`.

#### Conda

If you need to do update or add packages via `conda`, execute the following command **inside your jupyter notebook**:

```bash
import sys

# install a conda package in the current Jupyter kernel
!conda install --yes --prefix {sys.prefix} <package>
```

> _**note**_: the `!` notation is used to run `conda` directly as a shell command from the notebook. Also, take a look [here](https://jakevdp.github.io/blog/2017/12/05/installing-python-packages-from-jupyter/) to see why you should NOT use `!conda install --yes <package>`.

#### System

To add or update system packages, you will need `root` user permissions. To achieve this, use the following command:

```bash
# execute the container's shell
docker exec -it --user root tensorflow_notebook /bin/bash

# install a package to the system the container runs on
sudo apt install <package>
```

### Wrapping up

Once you're done, you may remove what was created by `up` with the following command:

```bash
# stop containers and removes containers, networks, volumes, and images created by `up`
docker-compose down
```
