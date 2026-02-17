# Project-Nova İndirme Rehberi

Aşağıda **Project-Nova** reposunu bilgisayarına indirmek için adım adım rehber var.

## 1) Git kurulu mu kontrol et
- Terminal aç.
- Şu komutu çalıştır:

```bash
git --version
```

- Sürüm görünüyorsa devam et.
- Komut bulunamazsa önce Git kur:
  - Windows: `winget install --id Git.Git -e`
  - macOS (Homebrew): `brew install git`
  - Ubuntu/Debian: `sudo apt update && sudo apt install -y git`

## 2) Projeyi indireceğin klasöre geç
- Örnek:

```bash
cd ~/Desktop
```

## 3) Project-Nova reposunu klonla
- Aşağıdaki komutla projeyi indir:

```bash
git clone https://github.com/Navjot-Singh7/Project-Nova.git
```

## 4) Proje klasörüne gir

```bash
cd Project-Nova
```

## 5) İndirme doğrulaması yap
- Dosyaları görmek için:

```bash
ls -la
```

- Git bağlantısını doğrulamak için:

```bash
git remote -v
```

## 6) (Opsiyonel) Güncel değişiklikleri çek
- Daha sonra projeyi güncellemek için:

```bash
git pull
```

---

## Sık karşılaşılan hatalar
- **`fatal: unable to access ...`**
  - İnternet, proxy veya kurumsal ağ kısıtı olabilir.
- **`Repository not found`**
  - URL'yi yanlış yazmış olabilirsin veya repo erişimi değişmiş olabilir.
- **`Permission denied (publickey)`**
  - SSH ile klonluyorsan SSH anahtarı ayarlı olmayabilir. HTTPS ile dene.

Repo linki: https://github.com/Navjot-Singh7/Project-Nova.git
