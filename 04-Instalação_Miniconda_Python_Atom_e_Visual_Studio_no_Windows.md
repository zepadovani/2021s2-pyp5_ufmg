## Instalação do *chocolatey*, *miniconda*/*Python* e *Atom*/*Visual Studio* no Windows

#### a) Instalação do **chocolatey**

Para um guia em vídeo sobre como instalar o *chocolatey*, ver:

[![Guia em vídeo - instalação chocolatey](https://img.youtube.com/vi/eHoh_ptUkmw/0.jpg)](https://www.youtube.com/watch?v=eHoh_ptUkmw)

1. Instalar a versão mais recente do *Powershell*, específica para seu sistema, a partir deste site:
[https://github.com/PowerShell/PowerShell/releases]

    obs: ao instalar, marque a opção que permite que adiciona o menu 'Open Here'/'Abrir Aqui' no Explorer.

2. Instalar *chocolatey* a partir do site: [https://chocolatey.org/install]

    2.1 Abrir PowerShell em modo admnistrador

    2.2 Executar antes o comando `Get-ExecutionPolicy`. Se retornar: `Restricted`, execute o comando `Set-ExecutionPolicy RemoteSigned `

    2.3 Executar o script de instalação do *chocolatey*:

    ```
    Set-ExecutionPolicy Bypass -Scope Process -Force; [System.Net.ServicePointManager]::SecurityProtocol = [System.Net.ServicePointManager]::SecurityProtocol -bor 3072; iex ((New-Object System.Net.WebClient).DownloadString('https://community.chocolatey.org/install.ps1'))
    ```

#### b) Instalação do Python a partir do miniconda

Para um guia em vídeo sobre como instalar o *miniconda* e o *Python* no windows, ver:

[![Guia em vídeo - instalação miniconda/python](https://img.youtube.com/vi/qt9UGKVSXnY/0.jpg)](https://www.youtube.com/watch?v=qt9UGKVSXnY)

1. Instalar o **miniconda** pelo PowerShell (em modo admnistrador):

    ```
    choco install miniconda3
    ```

2. Inicializar o conda para o PowerShell:

    ```
    conda init powershell
    ```

    obs: feche e reabra o shell (sempre em modo admnitrador) para que isso faça efeito

3. Criar um *ambiente*/*environment* Python utilizando o conda:

    ```
    conda create -n <nome_do_ambiente> python=<versão_do_python>
    ```

    **exemplo**:

    ```
    conda create -n mypy397 python=3.9.7
    ```

4. Ativar o ambiente criado:

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

#### c) Instalação e configuração do Atom e do Visual Studio

Para um guia em vídeo sobre como instalar e configurar o Atom e o Visual Studio, ver:

[![Guia em vídeo - instalação atom/vscode](https://img.youtube.com/vi/YxqoFTBYQLE/0.jpg)](https://www.youtube.com/watch?v=YxqoFTBYQLE)

1. Abrir PowerShell em modo admnistrador

2. Instalação do Atom:

    ```
    choco install atom -y
    ```

3. Instalação do Visual Studio Code:

    ```
    choco install vscode -y
    ```

4. Configuração Atom:

      Instalar pacotes:
      - `Hydrogen`
      - `script`

5. Configuração Visual Studio:

      Instalar pacote:
      - `Python`
