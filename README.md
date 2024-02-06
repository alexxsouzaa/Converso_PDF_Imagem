# Converso de PDF para imagem
Este é um simples script em Python que utiliza a biblioteca pdf2image para converter um arquivo PDF em imagens. 
O script extrai páginas do PDF e as salva como arquivos de imagem em um diretório especificado.

## Requisitos
Certifique-se de ter os seguintes requisitos instalados antes de executar o script:

* Python >= 3 ou Python <= 3.10
  
Use o comando abaixo para verificar a versão do Python:
```

Python --version

```

* Biblioteca pdf2image

Use o comando abaixo para instalar a biblioteca pdf2image:
```

pip install pdf2image

```

## Parâmetros
* pdf_path: O caminho do arquivo PDF que você deseja converter.
* output_diretorio: O diretório onde as imagens convertidas serão salvas. O diretório será criado se não existir.

## Uso
1. Clone o repositório ou baixe o script.
1. Certifique-se de ter o Python instalado.
1. Instale as dependências usando o comando mencionado acima.
1. Modifique a variável pdf_path para o caminho do seu arquivo PDF.
1. Execute o script.

## Exemplo
```
# Caminho do arquivo PDF
pdf_path = 'PDF_TESTE.pdf'

# Extrai o nome do arquivo
extensao_arquivo = pdf_path.find('.')
nome_arquivo = pdf_path[0:extensao_arquivo]

# Armazena o arquivo a ser convertido
images = convert_from_path(pdf_path)

# Diretório para onde o arquivo será exportado
output_diretorio = "./OUTPUT_FOLDER"

if not os.path.exists(output_diretorio):
    os.makedirs(output_diretorio)

for i in range(len(images)):
    # Salva a imagem
    images[i].save(os.path.join(output_diretorio, f'{nome_arquivo}_page{i}.jpg'), 'JPEG')

```
Certifique-se de substituir PDF_TESTE.pdf pelo caminho do seu próprio arquivo PDF.

Este é um script simples, mas pode ser útil para converter rapidamente páginas de PDF em imagens individuais. Sinta-se à vontade para personalizá-lo de acordo com suas necessidades.
