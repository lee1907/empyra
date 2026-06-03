# Empyra — Web sayfalari (GitHub Pages)

Bu klasor, Play Console'un istedigi HERKESE ACIK URL'leri saglar:
- `privacy.html`  -> Gizlilik Politikasi (TR + EN, tam Turkce karakterli)
- `terms.html`    -> Hizmet Sartlari (TR + EN)
- `index.html`    -> Basit acilis sayfasi (her ikisine link)

Oyun ici "Hakkinda > Gizlilik / Hizmet Sartlari > Cevrimici Oku" butonlari ve
Play Console gizlilik alani bu adreslere baglanir.

================================================================
## GitHub Pages ile yayinlama (kullanici: lee1907)
================================================================
Hedef URL'ler (kodda da bunlar tanimli):
  https://lee1907.github.io/empyra/privacy.html
  https://lee1907.github.io/empyra/terms.html

### Yontem A — Yeni "empyra" reposu (onerilen)
1. github.com > New repository > ad: `empyra` (Public).
2. Bu klasordeki 3 dosyayi (index.html, privacy.html, terms.html) reponun
   KOK dizinine yukle (surukle-birak veya `git push`).
3. Repo > Settings > Pages > Build and deployment:
     Source: "Deploy from a branch"
     Branch: `main`  /  Folder: `/ (root)`  > Save
4. 1-2 dakika sonra siteler yayinda:
     https://lee1907.github.io/empyra/privacy.html
     https://lee1907.github.io/empyra/terms.html

Komut satiriyla:
```
cd store/web
git init
git add index.html privacy.html terms.html
git commit -m "Empyra privacy + terms pages"
git branch -M main
git remote add origin https://github.com/lee1907/empyra.git
git push -u origin main
```
Sonra Settings > Pages adimini (3) yap.

### Yontem B — Mevcut bir repo + /docs klasoru
Dosyalari mevcut bir reponun `docs/` klasorune koyup Settings > Pages'te
Folder olarak `/docs` secersen URL su olur:
  https://lee1907.github.io/<repo-adi>/privacy.html
Bu durumda kodda PrivacyUrl/TermsUrl ve store belgelerindeki adresleri
buna gore guncellemeyi unutma.

================================================================
## NOT
================================================================
- Adres degisirse SU 3 yeri guncelle:
  1. LuminaBootstrap.cs  ->  PrivacyUrl / TermsUrl sabitleri
  2. store/PLAY-CONSOLE-FORMS.md (Privacy Policy URL satiri)
  3. store/RELEASE-STEPS.md (App content > Privacy policy adimi)
- Sayfa metnini guncellersen "Son guncelleme / Last updated" tarihini de yenile.
