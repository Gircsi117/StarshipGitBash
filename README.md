# Starship setup – Git Bash + Windows Terminal

## 1. Starship telepítése
```bash
winget install Starship.Starship
```

---

## 2. Nerd Font telepítése
1. Menj a [nerdfonts.com](https://www.nerdfonts.com) oldalra
2. Tölts le egyet (ajánlott: **JetBrainsMono Nerd Font** vagy **CascadiaCode Nerd Font**)
3. Csomagold ki, majd jobb klikk a `.ttf` fájlon → **Telepítés**
4. **Indítsd újra a gépet (csak ha nem működik)**

---

## 3. Windows Terminal beállítása
1. Nyisd meg a Windows Terminalt
2. Settings → Git Bash profil → **Appearance**
3. Font face → válaszd ki a telepített Nerd Fontot
4. Mentés

---

## 4. Starship aktiválása Git Bash-ben
Nyisd meg (vagy hozd létre) a `~/.bashrc` fájlt:
```bash
nano ~/.bashrc
```
Add hozzá a végéhez:
```bash
eval "$(starship init bash)"
```
Mentés (`Ctrl+O`, `Enter`, `Ctrl+X`), majd:
```bash
source ~/.bashrc
```

> **Megjegyzés:** Ha a Git Bash figyelmeztet hogy nincs `~/.bash_profile`, automatikusan létrehozza — ez normális, nem hiba.

---

## 5. Konfiguráció (opcionális)
A config fájl helye: `~/.config/starship.toml`

```bash
nano ~/.config/starship.toml
```

Preset alkalmazása (pl. tokyo-night):
```bash
starship preset tokyo-night -o ~/.config/starship.toml
```

Az összes elérhető preset listázása:
```bash
starship preset -l
```

Alapra visszaállítás (config törlése):
```bash
rm ~/.config/starship.toml
```

Teljes dokumentáció: [starship.rs/config](https://starship.rs/config/)