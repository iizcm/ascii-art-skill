# ASCII Art — Skill

Multiple tools for different ASCII art needs. All tools are local CLI programs or free REST APIs — no API keys required.

## Tool 1: Text Banners (pyfiglet — local)
Render text as large ASCII art banners. 571 built-in fonts.
```bash
pip install pyfiglet --break-system-packages -q
python3 -m pyfiglet "YOUR TEXT" -f slant
python3 -m pyfiglet "TEXT" -f doom -w 80
python3 -m pyfiglet --list_fonts
```
**Recommended fonts:** `slant` (clean), `doom` (bold), `big` (readable), `cyberlarge` (cyberpunk), `3-d` (3D effect).

## Tool 2: Text Banners (asciified API — remote)
Free REST API, 250+ FIGlet fonts. No install needed.
```bash
curl -s "https://asciified.thelicato.io/api/v2/ascii?text=Hello+World&font=Slant"
curl -s "https://asciified.thelicato.io/api/v2/fonts"
```

## Tool 3: Cowsay (Message Art)
Wrap text in speech bubble with ASCII character. 50+ characters.
```bash
cowsay "Hello World"
cowsay -f tux "Linux rules"
cowsay -b "Borg"  # =_= eyes
cowsay -l  # List all characters
```
Popular: `dragon`, `tux`, `vader`, `elephant`, `hellokitty`.

## Tool 4: Boxes (Decorative Borders)
Draw decorative ASCII borders around any text. 70+ designs.
```bash
echo "Hello World" | boxes
echo "Hello World" | boxes -d stone
echo "Hello World" | boxes -d unicornsay
boxes -l
```
Combine: `python3 -m pyfiglet "HERMES" -f slant | boxes -d stone`

## Tool 5: Toilet (Colored Text Art)
Like pyfiglet but with ANSI color effects.
```bash
toilet "Hello World"
toilet --gay "Rainbow!"
toilet --metal "Metal!"
toilet -F border "Bordered"
```

## Tool 6: Image to ASCII Art
Convert images (PNG, JPEG, GIF, WEBP) to ASCII art.
```bash
# Option A: ascii-image-converter (recommended)
ascii-image-converter image.png -C              # Color output
ascii-image-converter image.png -d 60,30        # Dimensions
ascii-image-converter image.png -b              # Braille

# Option B: jp2a (lightweight, JPEG only)
jp2a --width=80 image.jpg
jp2a --colors image.jpg
```

## Tool 7: Search Pre-Made ASCII Art
Search curated ASCII art from ascii.co.uk via curl.
```bash
curl -s 'https://ascii.co.uk/art/cat' -o /tmp/ascii_art.html
# Extract from <pre> tags using Python
```
Subjects: Animals (`cat`, `dog`, `horse`, `dragon`), Objects (`car`, `ship`, `guitar`), Nature (`tree`, `flower`, `sun`), Characters (`skull`, `robot`, `ninja`), Holidays (`christmas`, `halloween`).

## Tool 8: Fun ASCII Utilities
```bash
curl -s "qrenco.de/Hello+World"       # QR code as ASCII
curl -s "wttr.in/London"              # Weather with ASCII graphics
curl -s https://api.github.com/octocat # Random Octocat
```

## Unicode Character Palette (for custom art)
- **Box Drawing:** `╔ ╗ ╚ ╝ ║ ═ ╠ ╣ ╦ ╩ ╬ ┌ ┐ └ ┘ │ ─ ├ ┤ ┬ ┴ ┼ ╭ ╮ ╰ ╯`
- **Block Elements:** `░ ▒ ▓ █ ▄ ▀ ▌ ▐ ▖ ▗ ▘ ▝ ▚ ▞`
- **Geometric/Symbols:** `◆ ◇ ◈ ● ○ ◉ ■ □ ▲ △ ▼ ▽ ★ ☆ ✦ ✧ ◀ ▶ ◁ ▷ ⬡ ⬢ ⌂`

## Rules
- Max width: 60 chars per line (terminal-safe)
- Max height: 15 lines for banners, 25 for scenes
- Monospace only

## Decision Flow
1. Text banner → pyfiglet or asciified API
2. Fun message → cowsay
3. Decorative border → boxes
4. Specific thing → ascii.co.uk
5. Image to ASCII → ascii-image-converter or jp2a
6. QR code → qrenco.de
7. Weather/moon → wttr.in
8. Custom creative → LLM + Unicode palette
