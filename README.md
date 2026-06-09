# Copa do Mundo FIFA 2026 — PWA

## Como instalar no celular / desktop

### Android (Chrome)
1. Abra o `index.html` em um servidor web (ver abaixo)
2. Toque no botão **📲 Instalar App** no topo
3. Confirme a instalação — o ícone aparece na tela inicial

### iPhone / iPad (Safari)
1. Abra no Safari
2. Toque em **Compartilhar** → **Adicionar à Tela de Início**
3. Confirme

### Desktop (Chrome / Edge)
1. Abra no navegador
2. Clique no ícone de instalação na barra de endereço (ou botão no topo)

---

## Como servir localmente (necessário para PWA funcionar)

### Opção 1 — Python (já instalado no Mac/Linux)
```bash
cd copa2026
python3 -m http.server 8080
# Abrir: http://localhost:8080
```

### Opção 2 — Node.js
```bash
npx serve copa2026
```

### Opção 3 — VS Code
Instale a extensão **Live Server** e clique em "Go Live"

---

## Hospedagem gratuita (para acesso pelo celular de qualquer lugar)

### Netlify (recomendado, grátis)
1. Acesse netlify.com → **Add new site → Deploy manually**
2. Arraste a pasta `copa2026` → Pronto!
3. URL gerada automaticamente (ex: `copa2026-abc.netlify.app`)

### GitHub Pages
1. Suba a pasta para um repositório GitHub
2. Settings → Pages → Branch: main → /root
3. URL: `seuusuario.github.io/copa2026`

---

## Estrutura de arquivos
```
copa2026/
├── index.html          ← App principal
├── manifest.json       ← Configuração PWA
├── sw.js               ← Service Worker (offline)
├── icons/              ← Ícones para todos os tamanhos
│   ├── icon-72x72.png
│   ├── icon-96x96.png
│   ├── icon-128x128.png
│   ├── icon-144x144.png
│   ├── icon-152x152.png
│   ├── icon-192x192.png
│   ├── icon-384x384.png
│   ├── icon-512x512.png
│   └── icon-maskable-512x512.png
└── README.md
```

## Funcionalidades offline
- Todos os dados são salvos no **localStorage** do navegador
- Funciona 100% sem internet após o primeiro carregamento
- Service Worker garante cache de todos os recursos
