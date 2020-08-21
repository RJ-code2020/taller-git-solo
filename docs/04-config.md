---
id: 04-config
title: Configuración para despliegue
---

1. colocar los datos necesarios en el archivo `.gitlab.env` que se usarán para desplegar la pag web
```
URL=https://<gitlab-username>.gitlab.io
BASE_URL=/<project-name>/
PROJECT_NAME=<project-name>
ORGANIZATION_NAME=<gitlab-user>
```

2. reemplazar los datos del archivo `.env` con `.gitlab.env`

3. en el archibo `.gitlab-ci.yml`, cambiar el último comando del `script` colocando el nombre correcto del proyecto:
```yaml
image: node:lts

pages:
  script:
    - cd website
    - yarn install
    - yarn build
    - mv ./build/<project-name> ../public
  artifacts:
    paths:
      - public
  only:
    - master
```