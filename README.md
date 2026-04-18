# Write-Up · The Server from Hell

**TryHackMe · Abril 2026 · Juan Pablo**

---

## Como usar no GitHub Pages

1. Faça upload de todos os arquivos desta pasta para um repositório GitHub
2. Vá em **Settings → Pages → Source: Deploy from branch → main / root**
3. Acesse: `https://<seu-usuario>.github.io/<nome-do-repo>/writeup-the-server-from-hell.html`

## Estrutura

```
/
├── writeup-the-server-from-hell.html   ← write-up principal
├── 1776480*.png                        ← imagens do write-up
└── README.md                           ← este arquivo
```

## Flags

| # | Flag | Origem |
|---|------|--------|
| 1 | `thm{h0p3_y0u_l1k3d_th3_f1r3w4ll}` | flag.txt via NFS/zip |
| 2 | `thm{sh3ll_3c4p3_15_v3ry_1337}` | user.txt via reverse shell |
| 3 | `rootrootthm{w0w_n1c3_3sc4l4t10n}` | root.txt via tar + cap_dac_read_search |

## Técnicas

- Nmap SYN Stealth · Banner Grabbing · NFS Misconfiguration
- zip2john · John the Ripper · SSH Key Auth
- IRB Restricted Shell Escape · Ruby Reverse Shell
- Linux Capabilities · `getcap` · GTFOBins
