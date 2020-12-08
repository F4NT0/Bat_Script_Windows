# Como criar um Batch para windows

---

### Criando um Arquivo pelo Powershell

1. Abrimos o Powershell em um Diretório desejado
2. Utilizamos o seguinte comando do Powershell para criar um novo Arquivo do tipo `batch`:

```powershell
> New-Item './teste.bat' -ItemType File
```

### Escrevendo um Arquivo .bat

Podemos colocar qualquer comando em um .bat, onde `ECHO` serve para enviar texto para o Terminal, como no exemplo Abaixo:

```bat
@ECHO OFF
ECHO Congratulations! Your first batch file executed sucessfully.
PAUSE
```

### Rodando um Arquivo .bat no Powershell

Rodamos o arquivo com o seguinte comando de exemplo, usando o comando **Start-Process**:

```powershell
> Start-Process .\teste.bat
```

### Rodando um Arquivo .jar com .bat

1. Adicione no Diretório desejado o arquivo .jar que deseja iniciar.
2. No Arquivo .bat coloque o seguinte comando:

```bat
:: Arquivo Run_Project.bat
java -jar -Xmx1024m ".\grp-unificado-api-12.0-shaded.jar"
pause
```

3. Depois de escrever no Arquivo, abra o Powershell no Diretório e inicie o Arquivo com o seguinte comando:

```powershell
> Start-Process .\Run_Project.bat
```