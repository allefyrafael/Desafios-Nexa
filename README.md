# 🔍 IA na AWS: Processamento de Imagens e Texto  

🚀 Repositório com projetos que exploram **Inteligência Artificial na AWS**, aplicando **AWS Textract** e **AWS Rekognition** para análise de imagens, extração de informações e reconhecimento de padrões.  

📌 **Objetivo:** Criar soluções práticas que utilizam IA para interpretar textos e identificar rostos em imagens.  

---

## 📂 Projetos  

### 📄 OCR Lista Escolar  
📜 **Descrição:** Software que utiliza **AWS Textract** para extrair textos de imagens contendo listas de materiais escolares, organizando e estruturando as informações de forma automatizada.  

🛠 **Tecnologias:**  
- **AWS Textract** – Extração de texto de imagens  
- **Python & Boto3** – Integração com a API da AWS  
- **JSON** – Estruturação dos dados extraídos  
- **Gerenciamento IAM** – Controle de permissões na AWS  

🔍 **Desafios e Aprendizados:**  
✔️ Organização correta dos blocos de texto retornados pela API  
✔️ Manipulação de dados estruturados para facilitar o uso posterior  
✔️ Configuração segura de credenciais e permissões no IAM  

📸 **Exemplo de uso:**  
```python
import boto3

textract = boto3.client('textract')

with open('lista_escolar.jpg', 'rb') as image:
    response = textract.detect_document_text(Document={'Bytes': image.read()})

for item in response['Blocks']:
    if item['BlockType'] == 'LINE':
        print(item['Text'])
