# ASCII Art — Universal AI Agent Skill

<div align="center">

![MIT License](https://img.shields.io/badge/license-MIT-blue.svg)
![AI Agent Skill](https://img.shields.io/badge/universal--ai--agent--skill-FF6B35?style=for-the-badge)
![Category](https://img.shields.io/badge/category-creative-7C3AED?style=for-the-badge)

</div>

---

## English

### Overview

A universal AI agent skill for **ASCII art**. Provides structured guidance and multiple tools for creating text-based visual art — banners, decorative borders, character art, image-to-ASCII conversion, and more. All tools are local CLI programs or free REST APIs — no API keys required.

### When to Use This Skill

Use when the user wants text-based visual art: project name banners, decorative frames, ASCII characters (animals, objects), QR codes as ASCII, weather reports with ASCII graphics, or image-to-ASCII conversion.

### Quick Start

```bash
# Install recommended tools:
pip install pyfiglet --break-system-packages -q  # Text banners
sudo apt install cowsay boxes toilet toilet-fonts -y  # Character art & borders
sudo snap install ascii-image-converter  # Image to ASCII
```

### Available Tools

#### 1. Text Banners (pyfiglet)
Render text as large ASCII art banners. 571 built-in fonts.
```bash
python3 -m pyfiglet "YOUR TEXT" -f slant
python3 -m pyfiglet "TEXT" -f doom -w 80
python3 -m pyfiglet --list_fonts  # List all 571 fonts
```
**Recommended fonts:** `slant` (clean/modern), `doom` (bold/blocky), `big` (readable), `cyberlarge` (cyberpunk), `3-d` (3D effect).

#### 2. Text Banners (asciified API — remote)
Free REST API with 250+ FIGlet fonts. No install needed.
```bash
curl -s "https://asciified.thelicato.io/api/v2/ascii?text=Hello+World&font=Slant"
curl -s "https://asciified.thelicato.io/api/v2/fonts"  # List fonts
```

#### 3. Cowsay (Message Art)
Wrap text in fun ASCII characters with speech bubbles.
```bash
cowsay "Hello World"
cowsay -f tux "Linux rules"
cowsay -b "Borg"  # =_= eyes
cowsay -l  # List all 50+ characters
```
**Popular characters:** `dragon`, `tux`, `vader`, `elephant`, `hellokitty`, `stegosaurus`.

#### 4. Boxes (Decorative Borders)
Draw decorative ASCII art frames around any text. 70+ built-in designs.
```bash
echo "Hello World" | boxes
echo "Hello World" | boxes -d stone
echo "Hello World" | boxes -d unicornsay
boxes -l  # List all 70+ designs
```
**Combine with pyfiglet:** `python3 -m pyfiglet "HERMES" -f slant | boxes -d stone`

#### 5. Toilet (Colored Text Art)
Like pyfiglet but with ANSI color effects.
```bash
toilet "Hello World"
toilet --gay "Rainbow!"     # Rainbow coloring
toilet --metal "Metal!"     # Metallic effect
toilet -F border "Bordered" # Add border
```

#### 6. Image to ASCII Art
Convert images (PNG, JPEG, GIF, WEBP) to ASCII art.
```bash
# Option A: ascii-image-converter (recommended)
ascii-image-converter image.png -C              # Color output
ascii-image-converter image.png -d 60,30        # Set dimensions
ascii-image-converter image.png -b              # Braille characters

# Option B: jp2a (lightweight, JPEG only)
jp2a --width=80 image.jpg
jp2a --colors image.jpg
```

#### 7. Pre-made ASCII Art Search
Search curated ASCII art from ascii.co.uk.
```bash
curl -s 'https://ascii.co.uk/art/cat' -o /tmp/ascii_art.html
# Then extract from <pre> tags using Python
```
**Available subjects:** Animals (`cat`, `dog`, `horse`, `dragon`), Objects (`car`, `ship`, `guitar`), Nature (`tree`, `flower`, `sun`), Characters (`skull`, `robot`, `ninja`), Holidays (`christmas`, `halloween`).

#### 8. Fun ASCII Utilities
```bash
curl -s "qrenco.de/Hello+World"       # QR code as ASCII
curl -s "wttr.in/London"              # Weather with ASCII graphics
curl -s "wttr.in/Moon"                # Moon phase in ASCII
curl -s https://api.github.com/octocat # Random Octocat with quote
```

### Decision Flow
1. **Text banner** → pyfiglet (local) or asciified API (remote)
2. **Fun character message** → cowsay
3. **Decorative border** → boxes
4. **Art of a specific thing** → ascii.co.uk via curl
5. **Image to ASCII** → ascii-image-converter or jp2a
6. **QR code** → qrenco.de
7. **Weather/moon art** → wttr.in
8. **Custom creative** → LLM generation with Unicode palette

### Unicode Character Palette (for custom art)
- **Box Drawing:** `╔ ╗ ╚ ╝ ║ ═ ╠ ╣ ╦ ╩ ╬ ┌ ┐ └ ┘ │ ─ ├ ┤ ┬ ┴ ┼ ╭ ╮ ╰ ╯`
- **Block Elements:** `░ ▒ ▓ █ ▄ ▀ ▌ ▐ ▖ ▗ ▘ ▝ ▚ ▞`
- **Geometric/Symbols:** `◆ ◇ ◈ ● ○ ◉ ■ □ ▲ △ ▼ ▽ ★ ☆ ✦ ✧ ◀ ▶ ◁ ▷ ⬡ ⬢ ⌂`

### Rules
- Max width: 60 characters per line (terminal-safe)
- Max height: 15 lines for banners, 25 for scenes
- Monospace only: must render correctly in fixed-width fonts

---

## Bahasa Indonesia

### Ringkasan

Skill agen AI universal untuk **seni ASCII**. Memberikan panduan terstruktur dan berbagai alat untuk membuat seni visual berbasis teks — spanduk, bingkai dekoratif, karakter ASCII, konversi gambar ke ASCII, dan lainnya. Semua alat adalah program CLI lokal atau REST API gratis — tanpa kunci API.

### Kapan Menggunakan Skill Ini

Gunakan ketika pengguna ingin seni visual berbasis teks: spanduk nama proyek, bingkai dekoratif, karakter ASCII (hewan, objek), kode QR sebagai ASCII, laporan cuaca dengan grafis ASCII, atau konversi gambar ke ASCII.

### Mulai Cepat

```bash
# Instal alat yang direkomendasikan:
pip install pyfiglet --break-system-packages -q  # Spanduk teks
sudo apt install cowsay boxes toilet toilet-fonts -y  # Seni karakter & bingkai
sudo snap install ascii-image-converter  # Gambar ke ASCII
```

### Alat yang Tersedia

#### 1. Spanduk Teks (pyfiglet)
Render teks sebagai spanduk seni ASCII besar. 571 font bawaan.
```bash
python3 -m pyfiglet "TEKS ANDA" -f slant
python3 -m pyfiglet "TEKS" -f doom -w 80
python3 -m pyfiglet --list_fonts  # Daftar semua 571 font
```
**Font yang direkomendasikan:** `slant` (bersih/modern), `doom` (tebal/blok), `big` (mudah dibaca), `cyberlarge` (cyberpunk), `3-d` (efek 3D).

#### 2. Spanduk Teks (API asciified — remote)
API REST gratis dengan 250+ font FIGlet. Tidak perlu instalasi.
```bash
curl -s "https://asciified.thelicato.io/api/v2/ascii?text=Halo+Dunia&font=Slant"
curl -s "https://asciified.thelicato.io/api/v2/fonts"  # Daftar font
```

#### 3. Cowsay (Seni Pesan)
Bungkus teks dalam karakter ASCII lucu dengan gelembung percakapan.
```bash
cowsay "Halo Dunia"
cowsay -f tux "Aturan Linux"
cowsay -b "Borg"  # Mata =_=
cowsay -l  # Daftar semua 50+ karakter
```
**Karakter populer:** `dragon`, `tux`, `vader`, `elephant`, `hellokitty`, `stegosaurus`.

#### 4. Boxes (Bingkai Dekoratif)
Gambar bingkai seni ASCII dekoratif di sekitar teks apa pun. 70+ desain bawaan.
```bash
echo "Halo Dunia" | boxes
echo "Halo Dunia" | boxes -d stone
echo "Halo Dunia" | boxes -d unicornsay
boxes -l  # Daftar semua 70+ desain
```
**Gabungkan dengan pyfiglet:** `python3 -m pyfiglet "HERMES" -f slant | boxes -d stone`

#### 5. Toilet (Seni Teks Berwarna)
Seperti pyfiglet tetapi dengan efek warna ANSI.
```bash
toilet "Halo Dunia"
toilet --gay "Pelangi!"     # Pewarnaan pelangi
toilet --metal "Logam!"     # Efek logam
toilet -F border "Berbingkai" # Tambah bingkai
```

#### 6. Gambar ke Seni ASCII
Konversi gambar (PNG, JPEG, GIF, WEBP) ke seni ASCII.
```bash
# Opsi A: ascii-image-converter (direkomendasikan)
ascii-image-converter gambar.png -C              # Output berwarna
ascii-image-converter gambar.png -d 60,30        # Atur dimensi
ascii-image-converter gambar.png -b              # Karakter braille

# Opsi B: jp2a (ringan, hanya JPEG)
jp2a --width=80 gambar.jpg
jp2a --colors gambar.jpg
```

#### 7. Pencarian Seni ASCII Siap Pakai
Cari seni ASCII kurasi dari ascii.co.uk.
```bash
curl -s 'https://ascii.co.uk/art/kucing' -o /tmp/ascii_art.html
# Kemudian ekstrak dari tag <pre> menggunakan Python
```
**Subjek tersedia:** Hewan (`kucing`, `anjing`, `kuda`, `naga`), Objek (`mobil`, `kapal`, `gitar`), Alam (`pohon`, `bunga`, `matahari`), Karakter (`tengkorak`, `robot`, `ninja`), Liburan (`natal`, `halloween`).

#### 8. Alat Seni ASCII Seru
```bash
curl -s "qrenco.de/Halo+Dunia"       # Kode QR sebagai ASCII
curl -s "wttr.in/Jakarta"              # Cuaca dengan grafis ASCII
curl -s "wttr.in/Bulan"                # Fase bulan dalam ASCII
curl -s https://api.github.com/octocat # Octocat acak dengan kutipan
```

### Alur Keputusan
1. **Spanduk teks** → pyfiglet (lokal) atau API asciified (remote)
2. **Pesan karakter seru** → cowsay
3. **Bingkai dekoratif** → boxes
4. **Seni hal spesifik** → ascii.co.uk via curl
5. **Gambar ke ASCII** → ascii-image-converter atau jp2a
6. **Kode QR** → qrenco.de
7. **Seni cuaca/bulan** → wttr.in
8. **Kreatif kustom** → Pembuatan LLM dengan palet Unicode

### Palet Karakter Unicode (untuk seni kustom)
- **Gambar Kotak:** `╔ ╗ ╚ ╝ ║ ═ ╠ ╣ ╦ ╩ ╬ ┌ ┐ └ ┘ │ ─ ├ ┤ ┬ ┴ ┼ ╭ ╮ ╰ ╯`
- **Elemen Blok:** `░ ▒ ▓ █ ▄ ▀ ▌ ▐ ▖ ▗ ▘ ▝ ▚ ▞`
- **Simbol Geometris:** `◆ ◇ ◈ ● ○ ◉ ■ □ ▲ △ ▼ ▽ ★ ☆ ✦ ✧ ◀ ▶ ◁ ▷ ⬡ ⬢ ⌂`

### Aturan
- Lebar maks: 60 karakter per baris (aman terminal)
- Tinggi maks: 15 baris untuk spanduk, 25 untuk adegan
- Hanya monospace: harus merender dengan benar di font tetap-lebar
