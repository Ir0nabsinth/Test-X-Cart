# Test-X-Cart

### 1. Создаём репозиторий
`$ echo "# Test-X-Cart" >> README.md` - добавдяем заголовок **Test-X-Cart** в **README.md**

`$ git init` - инициализируем новый репозиторий

`$ git add README.md` - добавляем описание файла **README.md** в репозиторий

`$  git remote add origin` https://github.com/Ir0nabsinth/Test-X-Cart.git - добавляем удаленный репозиторий с именем **“origin”** в файл конфигурации Git

`$ git add id_rsa.pub` - добавляет файл с публичным ssh-ключом в репозиторий

`$ git commit -m "add ssh-key-pub"` - фиксируем изменение

`$ git push origin master` - отправляем локальный репозиторий на удаленный репозиторий, в ветку **"master"**

### 2. Создаём первую ветку
`$ git checkout -b first-branch` - создаём новую ветку **"first-branch"**

`$ git push origin first-branch` - отправляем локальный репозиторий на удаленный репозиторий, в ветку **"first-branch"**

### 3. Создаём вторую ветку
`$ git checkout -b second-branch` - создаём новую ветку **"second-branch"**

`$ git push origin second-branch` - отправляем локальный репозиторий на удаленный репозиторий, в ветку **"second-branch"**

### 4. Подготавливаем первую ветку к слиянию через `pull request`
`$ git checkout first-branch` - переходим на ветку **"first-branch"**

`$ nano id_rsa.pub` - открываем файл **"id_rsa.pub"** и вносим изменения 

`$ git add id_rsa.pub` - добавляем изменённый файл **"id_rsa.pub"** в репозиторий

`$ git commit -m "change id_rsa.pub"` - фиксируем внесённые изменения

`$ git push origin first-branch` - отправляем локальный репозиторий на удаленный репозиторий в ветку **"first-branch"**

### 5. Подготавливаем вторую ветку с конфликтом для `pull request`
`$ git checkout second-branch` - переходим на ветку **"second-branch"**

`$ nano id_rsa.pub` - открываем файл **"id_rsa.pub"** и вносим изменения

`$ git add id_rsa.pub` - добавляем изменённый файл **"id_rsa.pub"** в репозиторий

`$ git commit -m "change id_rsa.pub in second branch"` - фиксируем внесённые изменения

`$ git push origin second-branch` - отправляем локальный репозиторий на удаленный репозиторий в ветку **"second-branch"**
