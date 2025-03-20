# Git Komutları Rehberi

Bu rehber, git komutlarını adım adım açıklayan ve örneklerle gösteren kapsamlı bir Git kullanım kılavuzudur. Yeni başlayanlar için git komutlarını öğrenmek ve uygulamak için detaylı bir rehberdir.

## Adım 1: Yeni Bir Klasör Oluşturun ve Git Başlatın

```sh
# Yeni bir klasör oluşturun ve içine girin
mkdir my_project
cd my_project

# Git deposu başlatın
git init
```

## Adım 2: Dosyalar Ekleyin ve İlk Commit'i Yapın

```sh
# Örnek dosya ekleyin
echo "# My Project" > README.md
mkdir src
touch src/main.py

# Dosyaları izlemeye alın ve commit yapın
git add .
git commit -m "Initial commit"
```

## Adım 3: Uzak Depo (Remote Repository) Ekleyin ve İlk Push'u Yapın

```sh
# Uzak depoyu ekleyin
git remote add origin https://github.com/OmerFaruk-Celik/my_project.git

# Uzak depodaki değişiklikleri çekin ve rebase yapın
git pull origin main --rebase

# Değişiklikleri uzak depoya gönderin
git push -u origin main
```

## Git Komutları ve Örnek Kullanımları

### 1. `git status`

Mevcut çalışma dizininin durumunu gösterir.

```sh
git status
```

### 2. `git config`

Git kullanıcı ayarlarını yapılandırır.

```sh
git config --global user.email "youremail.com"
git config --global user.name "Your Name"
```

### 3. `git add`

Çalışma dizinindeki değişiklikleri indexe ekler.

```sh
git add .
git add --all
```

### 4. `git commit`

Değişiklikleri kaydeder.

```sh
git commit -m "Initial commit"
git commit --amend  # En son commit üzerinde değişiklik yapar
```

### 5. `git rm`

Dosyayı çalışma dizininden ve index'ten siler.

```sh
git rm <dosya_adi>
```

### 6. `git init --bare`

Yalın bir depo oluşturur.

```sh
git init --bare "ProjeAdi.git"
```

### 7. `git clone`

Uzak depoyu klonlar.

```sh
git clone https://github.com/OmerFaruk-Celik/my_project.git
```

### 8. `git push`

Değişiklikleri uzak depoya gönderir.

```sh
git push origin main
```

### 9. `git pull`

Değişiklikleri uzak depodan çeker.

```sh
git pull origin main
```

### 10. `git log`

Commit geçmişini gösterir.

```sh
git log
git log --oneline
git log -n 3  # Son 3 commit'i gösterir
```

### 11. `git revert`

Belirtilen commit'i geri alır.

```sh
git revert <commit_hash>
```

### 12. `git tag`

Version bilgisi ekler.

```sh
git tag -a v1.0.1 -m "1.0.1"
```

### 13. `git branch`

Yeni bir dal oluşturur veya dalları listeler.

```sh
git branch  # Tüm dalları listeler
git branch <yeni_dal>  # Yeni bir dal oluşturur
```

### 14. `git checkout`

Dallar arasında geçiş yapar veya belirli bir commit'e gider.

```sh
git checkout <dal_adi>
git checkout -b <yeni_dal>  # Yeni bir dal oluşturur ve geçiş yapar
```

### 15. `git merge`

İki dalı birleştirir.

```sh
git merge <dal_adi>
```

### 16. `git rebase`

Commit geçmişini yeniden düzenler.

```sh
git rebase <dal_adi>
```

### 17. `git reset`

Commit geçmişini geri alır veya dosyaları index'ten çıkarır.

```sh
git reset --hard <commit_hash>  # Commit geçmişini geri alır
git reset <dosya_adi>  # Dosyayı index'ten çıkarır
```

### 18. `git clean`

Çalışma dizinindeki izlenmeyen dosyaları siler.

```sh
git clean -f
```

### 19. `git stash`

Çalışma dizinindeki değişiklikleri geçici olarak saklar.

```sh
git stash
git stash pop  # Saklanan değişiklikleri geri getirir
```

### 20. `git show`

Belirli bir commit veya nesne hakkında bilgi gösterir.

```sh
git show <commit_hash>
```

### Örnek Senaryo

#### 1. Yeni Bir Proje Başlatma

```sh
mkdir my_project
cd my_project
git init
echo "# My Project" > README.md
mkdir src
touch src/main.py
git add .
git commit -m "Initial commit"
git remote add origin https://github.com/OmerFaruk-Celik/my_project.git
git push -u origin main
```

#### 2. Yeni Bir Dal Oluşturma ve Geliştirme

```sh
git checkout -b new_feature
echo "print('Hello, World!')" > src/main.py
git add src/main.py
git commit -m "Add main script"
git push origin new_feature
```

#### 3. Ana Dal ile Birleştirme

```sh
git checkout main
git pull origin main --rebase
git merge new_feature
git push origin main
```

Bu rehber, Git ile çalışırken ihtiyaç duyabileceğiniz temel komutları ve adımları kapsamaktadır. Daha fazla bilgi için Git dokümantasyonuna başvurabilirsiniz.
