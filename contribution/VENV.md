#### Para criar uma virtual environment e instalar as dependências listadas em um arquivo, siga os passos abaixo:

## 1. **Abra o Terminal ou Prompt de Comando**:

   Abra o terminal ou prompt de comando no seu sistema operacional e navegue para a pasta onde deseja criar a virtual environment.

## 2. **Crie a Virtual Environment**:

   Execute o comando apropriado para criar a virtual environment. Por exemplo:

   ```shell
   python3 -m venv venvs/venv
   ```

   Ou, se estiver em um ambiente onde `python` é a versão padrão:

   ```shell
   python -m venv venvs/venv
   ```

   Neste comando, a virtual environment é criada no diretório `venv` dentro do diretório `venvs`. Se preferir utilizar diretórios diferentes, basta alterar o caminho especificado no comando.

## 3. **Ative a Virtual Environment**:

   A forma de ativar a virtual environment varia conforme o sistema operacional:

   - **No Windows**:
     ```shell
     venvs\venv\Scripts\activate
     ```

   - **No macOS e Linux**:
     ```shell
     source venvs/venv/bin/activate
     ```

   Neste comando, a virtual environment está localizada na pasta `venv` dentro do diretório `venvs`. Se utiliza diretórios diferentes, basta alterar o caminho especificado no comando.

## 4. **Instale as Dependências**:

   Com a virtual environment ativada, você pode instalar as dependências listadas em um arquivo. Por exemplo:

   ```shell
   pip install -r requirements/requirements.txt
   ```

   Ou, para instalar pacotes mais específicos:

   ```shell
   pip install torch torchvision torchaudio --index-url https://download.pytorch.org/whl/cu117
   pip install -r requirements/requirements-google.txt
   ```

   Neste comando, os arquivos `requirements.txt` ou `requirements-google.txt` estão localizados na pasta `requirements`. Se seus arquivos estiverem em diretórios diferentes, basta alterar o caminho especificado no comando.

## 5. **Salve as Dependências**:

   Para salvar em um arquivo as dependências instaladas (isso irá sobrescrever o arquivo), utilize o seguinte comando:

   ```shell
   pip freeze > requirements/requirements.txt
   ```

   Neste comando, o arquivo `requirements.txt` é salvo dentro do diretório `venvs`. Se preferir utilizar diretórios e arquivos diferentes, basta alterar no comando.


### Após seguir esses passos, sua virtual environment estará pronta para uso, com todas as dependências instaladas. Lembre-se de ativar a virtual environment sempre que estiver trabalhando no projeto para garantir o uso das dependências corretas.

## 6. **Desative a Virtual Environment**:

   Caso não precise mais da virtual environment, você pode desativá-la com o seguinte comando, dependendo do seu sistema operacional:

   - **No Windows**:
     ```shell
     venv\Scripts\deactivate
     ```

   - **No macOS**:
     ```shell
     source venv/bin/deactivate
     ```

   - **No Linux**:
     ```shell
     deactivate
     ```

   Lembre-se de que o caminho depende da pasta onde a virtual environment foi criada e da pasta em que você está trabalhando.
