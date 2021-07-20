# Comandos GitFLow

![p](https://wac-cdn.atlassian.com/dam/jcr:a13c18d6-94f3-4fc4-84fb-2b8f1b2fd339/01%20How%20it%20works.svg?cdnVersion=1718)

## Inicio

### Iniciar git flow

```bash
git-flow init
```

## Feature

![imgfeature](https://wac-cdn.atlassian.com/dam/jcr:34c86360-8dea-4be4-92f7-6597d4d5bfae/02%20Feature%20branches.svg?cdnVersion=1718)

### Crear feature (se debe realizar git checkout develop antes)

```bash
git flow feature start {nombre feature}
```

### Finalizar freature

```bash
git flow feature finish {nombre feature}
```

### Publicar feature

```bash
git flow feature publish {nombre feature}
```

### Obtener feature

```bash
git flow feature pull origin {nombre feature}
```

## Release

![imgrelease](https://wac-cdn.atlassian.com/dam/jcr:8f00f1a4-ef2d-498a-a2c6-8020bb97902f/03%20Release%20branches.svg?cdnVersion=1718)

### Comenzar release

```bash
git flow release start {NOMBRE RELEASE} [BASE]
```

### Publicar release

```bash
git flow release publish {NOMBRE RELEASE}
```

### Track release

```bash
git flow release track {NOMBRE RELEASE}
```

### Finalizar y publicar release

```bash
git flow release finish {NOMBRE RELEASE}
```

## Hotfix

![imghotfix](https://wac-cdn.atlassian.com/dam/jcr:cc0b526e-adb7-4d45-874e-9bcea9898b4a/04%20Hotfix%20branches.svg?cdnVersion=1718)

### Comenzar hotfix

```bash
git flow hotfix start {NOMBRE VERSION} [BASENAME]
```

### Finalizar hotfix

```bash
git flow hotfix finish {NOMBRE VERSION}
```

## Tag

### Crear TAG

```bash
git tag -a v1.0 -m "Comentario que se le quiera dar"
```

### Ver TAG

```bash
git show v1.0
```

### Publicar TAG

```bash
git push origin  v1.0
```

### Ver lista de TAG

```bash
git tag
```

## Otros

### Limpiar repositorio local

```bash
git remote update origin --prune
```

### Mostrar lista de ramas

```bash
git branch -a
```