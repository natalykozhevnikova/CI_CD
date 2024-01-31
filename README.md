
## Задача:
Сделать локальный шаблон CI и отдельный репозиторий с шаблонами, подключить их к своему основному репозиторию через include




## Решение:
Создан локальный файл `local-smoke-tests.gitlab-ci.yml`

```yaml
smoke-test-job:
  script: echo "SMOKE"
```

Создан основной файл `.gitlab-ci.yml`

```yaml
include:
  - local: local-smoke-tests.gitlab-ci.yml
#  - remote: https://github.com/DeleteDone/CI-CD/blob/main/CI-CD_Seminar04/remote_included-file.yml
```

Файл с аналогичным содержанием есть в этом репозитории: `remote_included-file.yml`



Repository Seminar04
![repository](https://github.com/natalykozhevnikova/CI_CD/blob/main/VirtualBox_cibox_47.png)

Remote included file job
![remote included file job](https://github.com/natalykozhevnikova/CI_CD/blob/main/VirtualBox_cibox_01.png)

Pipeline passed
![pipeline passed](https://github.com/natalykozhevnikova/CI_CD/blob/main/VirtualBox_cibox_34.png)

