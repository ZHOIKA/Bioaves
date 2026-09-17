# BioAves Android

Aplicativo Android que abre o BioAves em uma WebView segura e integrada.

## Identificação

- Nome: `BioAves`
- Package: `com.bioaves.app`
- Site carregado: `https://bioaves.netlify.app/`
- Android mínimo: Android 8.0 (API 26)
- Target: Android 15 / API 35

## Recursos

- Interface em tela cheia de app, sem barra do navegador
- JavaScript e armazenamento web habilitados
- Cookies persistidos
- Navegação interna do BioAves dentro do app
- Links externos enviados para o navegador/aplicativo correspondente
- Botão Voltar do Android navega no histórico do site
- Indicador de carregamento
- Upload de imagens com:
  - galeria / arquivos
  - câmera
  - seleção múltipla quando o site solicitar
- HTTPS obrigatório
- Safe Browsing do WebView
- Deep link para `https://bioaves.netlify.app`

## Gerar o APK pelo Android Studio

1. Abra esta pasta no Android Studio.
2. Aguarde o Gradle sincronizar.
3. Use **Build > Build App Bundle(s) / APK(s) > Build APK(s)**.
4. O arquivo compilado pode ser renomeado para `BioAves.apk`.

## Gerar automaticamente pelo GitHub Actions

O projeto inclui `.github/workflows/build-apk.yml`.

Ao enviar o projeto para um repositório GitHub na branch `main`, o workflow:
1. instala Java e Android SDK;
2. compila o aplicativo;
3. publica o arquivo final `BioAves.apk` no artifact `BioAves`.

Também é possível rodar manualmente em **Actions > Build BioAves APK > Run workflow**.

## Observação

O conteúdo principal continua hospedado em `bioaves.netlify.app`. Assim, mudanças publicadas no site aparecem no app sem precisar gerar um novo APK, exceto quando houver mudanças nas funções nativas do aplicativo.
