# Project-Nova İndirme ve Çalıştırma Rehberi

Aşağıda **Project-Nova** reposunu bilgisayarına indirmek ve sunucuyu çalıştırmak için adım adım rehber var.

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

## 6) Sunucuyu çalıştırma (adım adım)
> Bu repo farklı teknolojiler kullanıyor olabilir. Önce proje tipini bul, sonra uygun komutu çalıştır.

### 6.1 Proje tipini bul

```bash
ls
```

Aşağıdaki dosyalara göre ilerle:
- `package.json` varsa: **Node.js** projesi
- `requirements.txt` veya `pyproject.toml` varsa: **Python** projesi
- `pom.xml` varsa: **Java (Maven)** projesi
- `build.gradle` varsa: **Java/Kotlin (Gradle)** projesi
- `Dockerfile` veya `docker-compose.yml` varsa: **Docker** ile çalıştırma seçeneği olabilir

### 6.2 Node.js ise
1. Node sürümünü kontrol et:

```bash
node -v
npm -v
```

2. Bağımlılıkları kur:

```bash
npm install
```

3. Geliştirme sunucusunu başlat:

```bash
npm run dev
```

4. Eğer `dev` scripti yoksa alternatif:

```bash
npm start
```

### 6.3 Python ise
1. Python sürümünü kontrol et:

```bash
python3 --version
```

2. Sanal ortam oluştur ve aktif et:

```bash
python3 -m venv .venv
source .venv/bin/activate
```

3. Bağımlılıkları kur:

```bash
pip install -r requirements.txt
```

4. Uygulamayı başlat (projeye göre değişebilir):

```bash
python app.py
```
veya
```bash
python manage.py runserver
```
veya
```bash
uvicorn main:app --reload
```

### 6.4 Docker varsa
1. Docker sürümünü kontrol et:

```bash
docker --version
```

2. `docker-compose.yml` varsa:

```bash
docker compose up --build
```

3. Sadece `Dockerfile` varsa:

```bash
docker build -t project-nova .
docker run -p 3000:3000 project-nova
```

## 7) Sunucunun çalıştığını doğrulama
- Terminalde genelde şu tarz bir çıktı görürsün: `listening on ...` / `running on ...`
- Tarayıcıdan şu adresleri dene:
  - `http://localhost:3000`
  - `http://localhost:5173`
  - `http://localhost:8000`
  - `http://localhost:8080`
- Hangi port yazıyorsa ona git.

## 8) (Opsiyonel) Güncel değişiklikleri çek
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
- **`npm ERR! missing script: dev`**
  - `npm start` dene veya `package.json` içindeki `scripts` alanını kontrol et.
- **`ModuleNotFoundError` / `No module named ...`**
  - Python bağımlılıkları kurulu olmayabilir, `pip install -r requirements.txt` çalıştır.

Repo linki: https://github.com/Navjot-Singh7/Project-Nova.git
