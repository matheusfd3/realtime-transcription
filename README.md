# Realtime Transcription

## Descrição

Este projeto captura o áudio do microfone em tempo real e transcreve.

## Requisitos

> **Nota:** Dependências adicionais podem ser necessárias. Caso apareça algum erro, tente instalá-las manualmente.

### 1. Python 3.12

Certifique-se de ter o Python 3.12 instalado em seu sistema.

### 2. Dependências do sistema (Linux)

```bash
sudo apt-get update
sudo apt-get install python3-dev portaudio19-dev python3-tk
```

### 3. FFmpeg

```bash
sudo apt update && sudo apt install ffmpeg
```

> **Nota:** A instalação do ffmpeg pode não ser realmente necessária para o funcionamento.

### 4. Dependências Python

```bash
pip install -r requirements.txt
```

## Como usar

1. Clone o repositório em sua máquina local:

```bash
git clone https://github.com/matheusfd3/realtime-transcription.git
```

2. Entre no diretório do projeto:

```bash
cd realtime-transcription
```

3. Verifique o índice do seu dispositivo de áudio e ajuste o `input_device_index` no arquivo `main.py`.

4. **Importante:** A transcrição está configurada para o idioma **inglês** por padrão.

   **Para alterar o idioma:**

   a. Abra o arquivo `main.py`

   b. Localize a seção `recorder_config` (próximo ao final do arquivo)

   c. Modifique os seguintes parâmetros:

   ```python
   'model': 'base',              # Remova o '.en' para suporte multilíngue
   'realtime_model_type': 'tiny', # Remova o '.en' para suporte multilíngue
   'language': 'pt',             # Altere para o código do idioma desejado
   ```

5. Execute o script:

```bash
python main.py
```

## Contribuição

Contribuições são bem-vindas! Se você encontrou um bug ou tem alguma sugestão para melhorar o projeto, sinta-se à vontade para abrir uma issue ou enviar um pull request.

## Autor

Este projeto foi desenvolvido por [matheusfd3](https://github.com/matheusfd3)
