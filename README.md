# GeradorSenha
Gerador de senha para estudos com electron js.

## comandos para iniciarlizar o projeto:
  - `npm init`
  - `npm install electron --save-dev`
  - `npm install`
  
## comando para execultar:

`npm start`

# Gerar Executável:

**Passo 1:** Definir os scripts de build no package.json
Abra o arquivo **package.json** e adicione os scripts para construir e executar o aplicativo. Por exemplo:
      
      "scripts": {
      <code>"scripts": {
        "start": "electron .",
        "build": "electron-builder"
      }

OBS: O script "start" é usado para iniciar o aplicativo durante o desenvolvimento e o script "build" é usado para fazer a release do executável.

**Passo 2:** Instalar as dependências para a release
Para fazer a release do executável, você precisa instalar o pacote **electron-builder**. Execute o seguinte comando no terminal:

- `npm install electron-builder --save-dev`

**Passo 3:** Configurar as opções de build
Crie um arquivo chamado **electron-builder.json** na raiz do seu projeto e configure as opções de build. Aqui está um exemplo básico:
        
        {
          "appId": "com.example.myapp",
          "productName": "MyApp",
          "directories": {
            "output": "dist"
          },
          "win": {
            "target": "nsis"
          },
          "mac": {
            "target": "dmg"
          },
          "linux": {
            "target": "AppImage"
          }
        }
        
OBS: Essas opções definem o nome do aplicativo, o ID, o diretório de saída e os formatos de distribuição para diferentes plataformas. Você pode ajustá-las de acordo com suas necessidades.

**Passo 4:** Fazer a release
Agora para fazer a release do executável. Basta executar o seguinte comando:
`npm run build`
