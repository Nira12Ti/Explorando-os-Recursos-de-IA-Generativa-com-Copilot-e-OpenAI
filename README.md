from PIL import Image
import pytesseract

# Caminho para o executável do Tesseract (deve ser instalado previamente)
caminho_tesseract = r"C:\Users\Python\AppData\Local\Programs\Tesseract-OCR"
pytesseract.pytesseract.tesseract_cmd = caminho_tesseract + r"\tesseract.exe"

# Carrega a imagem
imagem = Image.open("nome_da_imagem.jpg")

# Extrai o texto da imagem
texto_extraido = pytesseract.image_to_string(imagem, lang="por")

print(texto_extraido)
