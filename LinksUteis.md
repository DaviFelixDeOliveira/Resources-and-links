# `Links Úteis`


[Transcrever áudio em texto (Evernote)]("https://evernote.com/pt-br/ai-transcribe/audio-to-text")

---

[Separar voz e instrumental de algum áudio/música (MusicLab-VocalRemover)]("https://vocalremover.easeus.com/br/version-history/")

---

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

##### **Sintaxe básica**

1) **Baixar vídeo**

```
yt-dlp "Link do vídeo"
```
---
2) **Melhor qualidade disponível**

```
yt-dlp -f "bestvideo+bestaudio/best" "Link do vídeo"
```
---
3) **Escolher pasta específica**

```
yt-dlp -P "C:\Lugar\Do\Arquivo " Link do vídeo"
```
---

4) **Ver qualidades disponíveis**

```
yt-dlp -F "Link do vídeo"
```
---
5) **Baixar vídeo na melhor qualidade disponível**

```
yt-dlp -f "bestvideo+bestaudio/best" "Link do vídeo"
```
##### **4K**

```
yt-dlp -f "bestvideo[height<=2160]+bestaudio/best[height<=2160]" "Link do vídeo"
```

##### **1080p**

```
yt-dlp -f "bestvideo[height<=1080]+bestaudio/best[height<=1080]" "Link do vídeo"
```

##### **720p**

```
yt-dlp -f "bestvideo[height<=720]+bestaudio/best[height<=720]" "Link do vídeo"
```

---

6) **Melhor qualidade + áudio + MP4 + pasta específica + nome personalizado**

```
yt-dlp --no-playlist -f "bv*+ba/b" --merge-output-format mp4 -o "C:\Lugar\Do\Arquivo\NomeDoVideo.%(ext)s" "Link do vídeo"
```

7) **Baixar só áudio MP3**

```
yt-dlp -x --audio-format mp3 "Link do vídeo"
```

---

8) **Baixar legenda**

```
yt-dlp --write-subs --skip-download "Link do vídeo"
```

**Legenda automática:**
```
yt-dlp --write-auto-subs --skip-download "Link do vídeo"
```

9) **Baixar apenas um trecho do vídeo**

```js
yt-dlp --download-sections "*00:00:00-00:00:30" "Link do vídeo"

//Assim baixa apenas os 30 segundos iniciais
```


10) **Dar nome personalizado ao arquivo**

```
yt-dlp -o "MeuVideo.%(ext)s" "Link do vídeo"
```

11) **Instalar FFmpeg**
```
winget install Gyan.FFmpeg
```
12) **Atualizar yt-dlp**
```
yt-dlp -U
```

13) **Testar FFmpeg**
```
ffmpeg -version
```

14) **Onde os arquivos são salvos?**

Na pasta atual que você está do terminal