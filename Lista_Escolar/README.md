OCR Lista Escolar
Projeto desenvolvido para demonstrar a aplicação do AWS Textract na extração de texto a partir de imagens contendo listas de materiais escolares. Esse projeto explora o uso da AWS para reconhecimento óptico de caracteres (OCR) em documentos simples.

Minha Experiência no Projeto
Ao trabalhar neste projeto, pude aprofundar meu conhecimento no uso do AWS Textract para análise de documentos e extração de texto de imagens. A implementação envolveu a integração da API da AWS com Python, permitindo processar imagens automaticamente e armazenar os resultados em um arquivo JSON.

Durante o desenvolvimento, aprendi a configurar permissões no IAM, gerenciar exceções com boto3, e estruturar a extração de texto de forma eficiente. Um dos principais desafios foi garantir a correta leitura dos blocos de texto retornados pelo Textract, organizando-os em linhas para facilitar o uso posterior.

Este projeto se mostrou uma excelente oportunidade para trabalhar com processamento de documentos, manipulação de APIs da AWS e boas práticas no desenvolvimento em Python.

Pré-requisitos
Python (versão compatível com boto3)
uv (gerenciador de pacotes e ambiente)
Conta AWS com permissões para usar o serviço Textract
Configuração do Ambiente
É necessário configurar um usuário no IAM com acesso ao serviço Textract. Isso inclui a criação de credenciais com permissões adequadas para análise de documentos.

Instalação
Para instalar as dependências do projeto, utilize o comando:

sh
Copiar
Editar
uv install
Execução
O código processa uma imagem contendo uma lista de materiais escolares e extrai seu texto usando AWS Textract. Para rodar a aplicação, utilize:

sh
Copiar
Editar
uv run main.py
O resultado será salvo no arquivo response.json, e o texto extraído será exibido no terminal.