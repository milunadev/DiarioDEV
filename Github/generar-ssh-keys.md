# Guía Rápida para Generar Claves SSH para GitHub

Esta guía proporciona pasos concisos para generar una clave SSH en Windows y Mac, utilizada para la autenticación con GitHub.

## Windows

### Requisitos
- Git Bash (instalado con Git para Windows)

### Pasos
1. Abre Git Bash.
2. Genera una nueva clave SSH:
   ```bash
   ssh-keygen -t ed25519 -C "tu_email@example.com"
3. Agrega la clave al agente SSH.
```bash
eval $(ssh-agent -s)
ssh-add ~/.ssh/id_ed25519
```
4.3. Visualiza la clave y agregala a Github.
```bash
clip < ~/.ssh/id_ed25519.pub
```
## MAC

### Pasos
1. En la terminal genera una nueva clave SSH:
   ```bash
   ssh-keygen -t ed25519 -C "tu_email@example.com"
2. Agregar la clave al agente:
```bash
eval "$(ssh-agent -s)"
ssh-add -K ~/.ssh/id_ed25519
```
3. Visualiza la clave y agregala a Github.
```bash
pbcopy < ~/.ssh/id_ed25519.pub
```
Comandos unificados:
```bash
ssh-keygen -t ed25519 -C "tu_email@example.com"
eval "$(ssh-agent -s)"
ssh-add -K ~/.ssh/id_ed25519
pbcopy < ~/.ssh/id_ed25519.pub
```