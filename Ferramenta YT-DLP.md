
## **`YT-DLP`**

é uma ferramenta de terminal para baixar vídeos, áudios, legendas e playlists de vários sites.

Funciona com:

- YouTube
- TikTok
- Instagram
- X/Twitter
- Facebook
- Twitch
- Reddit
- SoundCloud
etc.

---

## **`Configuração recomendada para YouTube`**

##### **Instalar Node.js**

https://nodejs.org/

---

##### **Exportar cookies do navegador**

Extensão Chrome:

https://chromewebstore.google.com/detail/get-cookiestxt-locally/njabckikapfpffapmjgojcnbfjonfjfg

---

##### **Salvar cookies**

Salvar o arquivo exportado como:

```text
C:\Users\Davi\Downloads\cookies.txt
```

---

##### **Comando base recomendado para YouTube**

```js
yt-dlp --js-runtimes "node:C:\Program Files\nodejs\node.exe" --cookies "C:\Users\Davi\Downloads\cookies.txt" "LINK_DO_VIDEO"
```

---

##### **Sintaxe básica**

1) **Baixar vídeo**

```js
yt-dlp --js-runtimes "node:C:\Program Files\nodejs\node.exe" --cookies "C:\Users\Davi\Downloads\cookies.txt" "Link do vídeo"
```

---

2) **Escolher pasta específica**

```js
yt-dlp --js-runtimes "node:C:\Program Files\nodejs\node.exe" --cookies "C:\Users\Davi\Downloads\cookies.txt" -P "C:\Lugar\Do\Arquivo" "Link do vídeo"
```

---

3) **Ver qualidades disponíveis**

```js
yt-dlp --js-runtimes "node:C:\Program Files\nodejs\node.exe" --cookies "C:\Users\Davi\Downloads\cookies.txt" -F "Link do vídeo"
```

---

4) **Baixar vídeo na melhor qualidade disponível**

```js
yt-dlp --js-runtimes "node:C:\Program Files\nodejs\node.exe" --cookies "C:\Users\Davi\Downloads\cookies.txt" -f "bestvideo+bestaudio/best" "Link do vídeo"
```

##### **4K**

```js
yt-dlp --js-runtimes "node:C:\Program Files\nodejs\node.exe" --cookies "C:\Users\Davi\Downloads\cookies.txt" -f "bestvideo[height<=2160]+bestaudio/best[height<=2160]" "Link do vídeo"
```

##### **1080p**

```js
yt-dlp --js-runtimes "node:C:\Program Files\nodejs\node.exe" --cookies "C:\Users\Davi\Downloads\cookies.txt" -f "bestvideo[height<=1080]+bestaudio/best[height<=1080]" "Link do vídeo"
```

##### **720p**

```js
yt-dlp --js-runtimes "node:C:\Program Files\nodejs\node.exe" --cookies "C:\Users\Davi\Downloads\cookies.txt" -f "bestvideo[height<=720]+bestaudio/best[height<=720]" "Link do vídeo"
```

---

5) **Melhor qualidade + áudio + MP4 + pasta específica + nome personalizado**

```js
yt-dlp --js-runtimes "node:C:\Program Files\nodejs\node.exe" --cookies "C:\Users\Davi\Downloads\cookies.txt" --no-playlist -f "bv*+ba/b" --merge-output-format mp4 -o "C:\Lugar\Do\Arquivo\NomeDoVideo.%(ext)s" "Link do vídeo"
```

---

6) **Baixar só áudio MP3**

```js
yt-dlp --js-runtimes "node:C:\Program Files\nodejs\node.exe" --cookies "C:\Users\Davi\Downloads\cookies.txt" -x --audio-format mp3 "Link do vídeo"
```

---

7) **Baixar legenda**

```js
yt-dlp --js-runtimes "node:C:\Program Files\nodejs\node.exe" --cookies "C:\Users\Davi\Downloads\cookies.txt" --write-subs --skip-download "Link do vídeo"
```

**Legenda automática:**

```js
yt-dlp --js-runtimes "node:C:\Program Files\nodejs\node.exe" --cookies "C:\Users\Davi\Downloads\cookies.txt" --write-auto-subs --skip-download "Link do vídeo"
```

**Como ver quais legendas existem?**

```js
yt-dlp --js-runtimes "node:C:\Program Files\nodejs\node.exe" --cookies "C:\Users\Davi\Downloads\cookies.txt" --list-subs "Link do vídeo"
```

Isso mostra:
- idiomas disponíveis
- manual ou automática
- formatos

---

8) **Baixar apenas um trecho do vídeo**

```js
yt-dlp --js-runtimes "node:C:\Program Files\nodejs\node.exe" --cookies "C:\Users\Davi\Downloads\cookies.txt" --download-sections "*00:00:00-00:00:30" "Link do vídeo"

// Assim baixa apenas os 30 segundos iniciais
```

---

9) **Dar nome personalizado ao arquivo**

```js
yt-dlp --js-runtimes "node:C:\Program Files\nodejs\node.exe" --cookies "C:\Users\Davi\Downloads\cookies.txt" -o "MeuVideo.%(ext)s" "Link do vídeo"
```

---

10) **Instalar FFmpeg**

```js
winget install Gyan.FFmpeg
```

---

11) **Atualizar yt-dlp**

```js
yt-dlp -U
```

---

12) **Testar FFmpeg**

```js
ffmpeg -version
```

---

13) **Onde os arquivos são salvos?**

Na pasta atual que você está do terminal

---

14) **Converter vídeo para formato compatível (Holyrics, projetor, TV, etc)**

```js
ffmpeg -i "VideoOriginal.mp4" -c:v libx264 -pix_fmt yuv420p -preset medium -crf 23 -c:a aac -b:a 192k "VideoConvertido_OK.mp4"

// Aqui o vídeo fica salvo na pasta em que você está (abrindo cmd o padrão é C:\Users\Davi )
```

---

15) **Baixar vídeo compatível com Holyrics (sem converter depois)**

```js
yt-dlp --js-runtimes "node:C:\Program Files\nodejs\node.exe" --cookies "C:\Users\Davi\Downloads\cookies.txt" -f "bv*[vcodec^=avc1]+ba[acodec^=mp4a]/b[ext=mp4]" --merge-output-format mp4 "LINK_DO_VIDEO"
```

---

16) **Baixar thumbnail/capa do vídeo**

```js
yt-dlp --js-runtimes "node:C:\Program Files\nodejs\node.exe" --cookies "C:\Users\Davi\Downloads\cookies.txt" --write-thumbnail --skip-download "Link do vídeo"
```

---

17) **Baixar áudio em melhor qualidade**

```js
yt-dlp --js-runtimes "node:C:\Program Files\nodejs\node.exe" --cookies "C:\Users\Davi\Downloads\cookies.txt" -f "bestaudio" "Link do vídeo"
```

---

18) **Baixar áudio já em AAC (melhor qualidade)**

```js
yt-dlp --js-runtimes "node:C:\Program Files\nodejs\node.exe" --cookies "C:\Users\Davi\Downloads\cookies.txt" -f "bestaudio[acodec^=mp4a]/bestaudio" -x --audio-format aac --audio-quality 0 "Link do vídeo"
```

---

19) **Extrair áudio de um vídeo com FFmpeg**

```js
ffmpeg -i "Video.mp4" -vn -c:a mp3 "Audio.mp3"
```