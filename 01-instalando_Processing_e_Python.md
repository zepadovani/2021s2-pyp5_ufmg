# Instalando Python e Processing

Antes de começarmos, é importante que você tenha Python e Processing instalados no seu computador.

## Processing

O *Processing*, atualmente, já tem uma versão 4 (atualmente em estágio beta) disponibilizada. No entanto, utilizaremos a versão **3.5.4**. Isso se deve ao fato de que essa é, no momento, a última versão do *Processing* que tem habilitado o **modo Python** e que permite usar a sintaxe da linguagem *Python* para criar sketches de em Processing. Ainda que os sketches em *modo Python* sejam muito semelhantes àqueles utilizados nos modos *Java* e *p5.js* (*javascript*), do ponto de vista pedagógico tentaremos utilizar ao máximo códigos em Python: isso permitirá criar uma maior familiaridade com a sintaxe dessa linguagem o que, em um segundo momento, possibilitará usar o próprio *Python* (fora do ambiente *Processing*) como ferramenta de criação de música e arte digital.

Para instalar o Processing no seu computador, basta ir ao endereço [https://processing.org/download](https://processing.org/download) e selecionar a opção "3.5.4 (January 17, 2020)" correspondente ao seu sistema operacional.

As instruções de instalação são autoexplicativas.

Para um guia em vídeo sobre como instalar o *Processing* nos sistemas Windows, macOS e Linux (Ubuntu), ver:

windows:<br/>
[![2 - windows - Instalação do Processing](https://img.youtube.com/vi/rT-xn5wHVb8/0.jpg)](https://www.youtube.com/watch?v=rT-xn5wHVb8)

macOS:<br/>
[![2 - macOS - Instalação do Processing](https://img.youtube.com/vi/W4iUkXINz1Y/0.jpg)](https://www.youtube.com/watch?v=W4iUkXINz1Y)

linux/Ubuntu:<br/>
[![2 - linux/Ubuntu - Instalação do Processing](https://img.youtube.com/vi/MCdLZZfcT74/0.jpg)](https://www.youtube.com/watch?v=MCdLZZfcT74)

---

## Python

Para a instalação do Python, utilizaremos uma série de ferramentas que dependem do seu sistema operacional. Por esse motivo, há um guia, abaixo, para cada sistema operacional: **macOS**, **Windows 10** e **Linux/Ubuntu**. Para outros sistemas Linux ou versões específicas do macOS ou do Windows, podem ser necessários alguns ajustes (nesse caso, conversaremos durante as aulas).

Para os ambientes **Windows** e **macOS**, o passo-a-passo inclui a instalação de *Gerenciadores de Pacote*. São programas que facilitam bastante o processo de instalação de aplicativos, bibliotecas e ferramentas computacionais, permitindo controlar de maneira mais objetiva as dependências e especificidades de determinadas instalações. No caso do Windows, utilizaremos o *chocolatey*. Para o macOS, utilizaremos o *homebrew*. Distribuições linux já vêm com seus próprios gerenciadores, o que dispensa um guia específico.

### 1.1 Windows

#### a) Instalação do **chocolatey** [Windows]

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

#### b) Instalação do Python a partir do miniconda [Windows]

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

#### c) Instalação e configuração do Atom e do Visual Studio [Windows]

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

---

### 1.2 macOS

#### a) Instalação do **homebrew** [macOS]

Para um guia em vídeo sobre como instalar o *homebrew*, ver:

[![Guia em vídeo - instalação homebrew](https://img.youtube.com/vi/cI1dQXoZeqA/0.jpg)](https://www.youtube.com/watch?v=cI1dQXoZeqA)

1. [opcional] Instalar o iTerm:

    Baixar e instalar o aplicativo a partir do endereço: [https://iterm2.com/]

2. Abrir o terminal (o iTerm ou o Terminal, do próprio macOS)

3. Copiar o script de instalação do homebrew no site [https://brew.sh/]

4. Colar no terminal e executar para realizar a instalação:

    ```
    /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
    ```


#### b) Instalação do Python a partir do miniconda [macOS]

Para um guia em vídeo sobre como instalar o *miniconda* e o *Python* no macOS, ver:

[![Guia em vídeo - instalação miniconda/python](https://img.youtube.com/vi/cisrgY2G5IE/0.jpg)](https://www.youtube.com/watch?v=cisrgY2G5IE)

1. Instalar o **miniconda** pelo terminal utilizando o homebrew:

    ```
    brew install --cask miniconda
    ```

2. Inicializar o conda para o terminal em uso:

    ```
    conda init "$(basename "${SHELL}")"
    ```

    obs: feche e reabra o shell para que isso faça efeito

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


#### c) Instalação e configuração do Atom e do Visual Studio [macOS]

Para um guia em vídeo sobre como instalar e configurar o Atom e o Visual Studio, ver:

[![Guia em vídeo - instalação atom/vscode](https://img.youtube.com/vi/sZ9efYWqpE8/0.jpg)](https://www.youtube.com/watch?v=sZ9efYWqpE8)

1. Abrir o Terminal/iTerm

2. Instalação do Atom:

    ```
    brew install --cask atom
    ```

3. Instalação do Visual Studio Code:

    ```
    brew install --cask visual-studio-code
    ```    

4. Configuração Atom:

      Instalar pacotes:
      - `Hydrogen`
      - `script`

5. Configuração Visual Studio:

      Instalar pacote:
      - `Python`

---
### 1.3 Linux/Ubuntu

#### a) Instalação do Python a partir do miniconda [linux]

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


#### b) Instalação e configuração do Atom e do Visual Studio [Linux/Ubuntu]

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
