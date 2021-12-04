## Instalação do *miniconda*/*Python* e *Atom*/*Visual Studio* no Linux/Ubuntu

#### a) Instalação do Python a partir do miniconda

Para um guia em vídeo sobre como instalar o *miniconda* e o *Python* no Linux/Ubuntu, ver:

[![Guia em vídeo - instalação miniconda/python](https://img.youtube.com/vi/Tk-B6Nm8qOY/0.jpg)](https://www.youtube.com/watch?v=Tk-B6Nm8qOY)

1. Ir ao site docs.conda.io e, no menu lateral, seguir o caminho `Miniconda > Linux Installers` e encontrar a versão específica para seu processador (em geral, `Python 3.9 / Miniconda3 Linux 64-bit`)

2. Rodar o script de instalação e seguir instruções:

    ```
    bash ./Miniconda3-py39-xxxxxx.sh
    ```

3. Durante a instalação, marque 'yes' para a pergunta sobre inicializar o conda. Caso contrário, será necessário executar o comando `conda init` posteriormente utilizando o comando abaixo:

    ```
    conda init "$(basename "${SHELL}")"
    ```

    obs: feche e reabra o terminal para que a inicialização tenha efeito

4. Criar um *ambiente*/*environment* Python utilizando o conda:

    ```
    conda create -n <nome_do_ambiente> python=<versão_do_python>
    ```

    **exemplo**:

    ```
    conda create -n mypy397 python=3.9.7
    ```

5. Ativar o ambiente criado:

    ```
    conda activate mypy397
    ```

5. Intalação do Jupyter

    ```
    pip install jupyter
    ```

6. Configurar o kernel Jupyter (que possibilita utilizarmos o ambiente criado em modo interativo):

    ```
    python -m ipykernel install --user --name mypy397 --display-name "Python 3.9.7 - mypy397/conda"
    ```

7. Testando/rodando o Jpyter:

    ```
    jupyter notebook
    ```

8. Instalação de pacotes (exemplo com `numpy`):

    ```
    pip install numpy
    ```


#### b) Instalação e configuração do Atom e do Visual Studio 

Para um guia em vídeo sobre como instalar e configurar o Atom e o Visual Studio, ver:

[![Guia em vídeo - instalação atom/vscode](https://img.youtube.com/vi/I_fc9GvOAQE/0.jpg)](https://www.youtube.com/watch?v=I_fc9GvOAQE)

1. Abrir a loja de aplicativos do sistema

2. Procurar por Atom e instalar.

3. Procurar por Visual Studio e instalar.

4. Configuração Atom:

    Instalar pacotes:
    - `Hydrogen`
    - `script`

5. Configuração Visual Studio:

    Instalar pacote:
    - `Python`
