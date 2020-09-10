# PyInstaller-Windows-appdata-roaming
PyInstaller Windows appdata/roaming | C:\Users\guilh\AppData\Roaming

#Corrige erros de importação do PyInstaller
- Colocar os a pasta pyinstaller inteira na pasta C:\Users\guilh\AppData\Roaming


#Atualizar o setuptools:
```pip install -U setuptools```


#Somente em caso de erros com pytest remover o pacote e o resintalar novamente:
```pip uninstall pytest```
```pip install pytest```

#Caso ainda não instale:
```pip install pyinstaller==4.0 --no-build-isolation```

#Comando utilizado para compilar este programa:
```pyinstaller --onefile --noconsole main.py  --hidden-import PyQt5.sip```

#Comando para remover o console e por um icone:
```pyinstaller -F --noconsole  -i favicon.ico```

#Instalação do pyinstaller direto da fonte, como comunidade recomenda:
```pip install https://github.com/pyinstaller/pyinstaller/archive/develop.zip```

#Outros comandos que podem auxiliar futuramente com o pyinstaller:
```pyinstaller --onefile --hidden-import theMissingModule main.py```
```pyinstaller --onefile --windowed```


#Mais informações sobre o arquivo spec:
1. Insira todos os arquivos py necessários para que seu código seja executado na primeira lista dentro do Analysis
por exemplo: Analysis(['file1.py', 'file2.py', 'file3.py'],
2. Insira todos os arquivos de dados necessários na lista de dados (dentro do Analysis) no arquivo spec. Cada entrada será uma tupla. O primeiro elemento na tupla será o caminho para o recurso e a segunda entrada será o nome da pasta na saída.
Por exemplo: datas=[('csv\\', 'csv'), ('plotly-latest.min.js', '.')],
