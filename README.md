Задача: Сделать локальный шаблон CI и отдельный репозиторий с шаблонами, подключить их к своему основному репозиторию через include

Решение:
Создан локальный файл local-smoke-tests.gitlab-ci.yml
smoke-test-job:
  script: echo "SMOKE"
smoke-test-job:
  script: echo "SMOKE"
Создан основной файл .gitlab-ci.yml

include:
  - local: local-smoke-tests.gitlab-ci.yml
#  - remote: https://github.com/DeleteDone/CI-CD/blob/main/CI-CD_Seminar04/remote_included-file.yml
Файл с аналогичным содержанием, что и у Максима, есть в этом репозитории: remote_included-file.yml
