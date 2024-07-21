# Git Cheatsheet (Fundamentos)

Esta hoja de referencia es una lista de nuestros comandos de Git más utilizados y contiene información útil para aquellos que están comenzando.

_¿Quieres aprender más sobre el terminal? Hay una lista de nuestros comandos y atajos más utilizados en el [Terminal de macOS](https://github.com/0nn0/terminal-mac-cheatsheet/tree/master/Español)._

## Glosario

| Palabra clave              | Descripción                                                                                                    |
| -------------------------- | -------------------------------------------------------------------------------------------------------------- |
| git                        | Sistema de control de versiones distribuido de código abierto usado para almacenar código en repositorios      |
| GitHub, GitLab y Bitbucket | Plataformas para hospedar y colaborar en repositorios de Git                                                   |
| staging                    | Archivos o directorios que deseas preparar para el _commit_                                                    |
| commit                     | Guarda todos los archivos o directorios preparados en tu repositorio local                                     |
| branch                     | Crea una línea de desarrollo independiente para que las características puedan desarrollarse de manera aislada |
| clone                      | Clona los _commits_ y las _branches_ de la versión remota del repositorio a una nueva versión local            |
| remote                     | Versión remota común a todos los colaboradores                                                                 |
| fork                       | Copia un repositorio perteneciente a otro usuario creando un repositorio en tu cuenta                          |
| pull request               | Solicita la fusión de tus contribuciones a un repositorio                                                      |
| HEAD                       | Representa tu posición en el directorio de trabajo actual                                                      |

## Configuración

| Comando                                  | Descripción                                                                  |
| ---------------------------------------- | ---------------------------------------------------------------------------- |
| `git config --global user.name [nombre]` | Establece el nombre del autor a ser usado en todos los _commits_             |
| `git config --global user.email [email]` | Establece el correo electrónico del autor a ser usado en todos los _commits_ |
| `git config color.ui true`               | Activa la coloración de la UI del terminal                                   |

## Comandos Principales

| Comando                     | Descripción                                                                                  |
| --------------------------- | -------------------------------------------------------------------------------------------- |
| `git init [directorio]`     | Crea un nuevo repositorio local                                                              |
| `git clone [repo]`          | Crea una copia local del repositorio remoto                                                  |
| `git add [directorio]`      | Prepara el directorio para el _commit_                                                       |
| `git add [archivo]`         | Prepara el archivo para el _commit_                                                          |
| `git add -A`                | Prepara todos los archivos modificados para el _commit_                                      |
| `git add .`                 | Prepara los archivos nuevos y los modificados, ignorando los eliminados, para el _commit_    |
| `git add -u`                | Prepara los archivos eliminados y los modificados, ignorando los nuevos, para el _commit_    |
| `git commit -m "[mensaje]"` | _Commitea_ todos los archivos y directorios preparados para el _commit_                      |
| `git status`                | Muestra el estado de los archivos o directorios como no rastreados, modificados o preparados |

## Sincronización de Cambios

| Comando     | Descripción                                                                                |
| ----------- | ------------------------------------------------------------------------------------------ |
| `git fetch` | Descarga todo el historial de las _branches_ remotas                                       |
| `git merge` | Fusiona la _branch_ remota en la _branch_ local                                            |
| `git pull`  | Actualiza la _branch_ local con los nuevos _commits_ de la _branch_ remota correspondiente |
| `git push`  | Envía todos los _commits_ locales al repositorio remoto                                    |

_Consejo: `git pull` es la combinación de `git fetch` y `git merge`_

## Deshacer Cambios

| Comando                     | Descripción                                                                           |
| --------------------------- | ------------------------------------------------------------------------------------- |
| `git checkout -- [archivo]` | Sustituye el archivo por el contenido de la _HEAD_                                    |
| `git revert [commit]`       | Crea un nuevo _commit_ que deshace los cambios hechos en [commit]                     |
| `git reset [archivo]`       | Elimina el [archivo] del área de preparación                                          |
| `git reset --hard HEAD`     | Elimina todos los cambios locales en el directorio de trabajo actual                  |
| `git reset --hard [commit]` | Restablece el _HEAD_ al _commit_ anterior y descarta todos los cambios desde entonces |

## Branches

| Comando                    | Descripción                                       |
| -------------------------- | ------------------------------------------------- |
| `git branch [branch]`      | Crea una nueva _branch_                           |
| `git checkout [branch]`    | Cambia a esa _branch_                             |
| `git checkout [branch] -b` | Crea y cambia a una nueva _branch_                |
| `git merge [branch]`       | Fusiona la _branch_ [branch] a la _branch_ actual |
| `git branch -d [branch]`   | Elimina la _branch_                               |
| `git push origin [branch]` | Envía la _branch_ al repositorio remoto           |
| `git branch`               | Lista las _branches_ locales                      |
| `git branch -r`            | Lista las _branches_ remotas                      |
| `git branch -a`            | Lista las _branches_ locales y remotas            |

## Historial

| Comando                     | Descripción                                                              |
| --------------------------- | ------------------------------------------------------------------------ |
| `git log`                   | Lista el historial de versiones de la _branch_ actual                    |
| `git log --author=[nombre]` | Lista el historial de versiones de la _branch_ actual filtrado por autor |
| `git log --oneline`         | Lista el historial de versiones de la _branch_ actual de forma compacta  |
| `git show [commit]`         | Muestra los metadatos y cambios de contenido de un _commit_ específico   |
| `git blame [archivo]`       | Muestra quién hizo cambios en un archivo y cuándo se hicieron            |

## Gitignore

Añadir el archivo reservado para el sistema `.gitignore` a tu directorio permite que optes por la exclusión de ciertos archivos de futuros _commits_. Este archivo debe colocarse siempre en la raíz de tu repositorio.

Se nota que mucha gente suele excluir cachés de dependencias, como `node_modules`, archivos de sistema, como `.DS_Store`, entre otros.

Puedes ver el archivo `.gitignore` [de este repositorio](https://github.com/0nn0/git-basics-cheatsheet/blob/master/.gitignore) o [más ejemplos](https://github.com/github/gitignore) de GitHub.

## Plataformas

Las siguientes plataformas son ejemplos que pueden usarse para alojar tus repositorios.

| Plataforma                         | Precio |
| ---------------------------------- | ------ |
| [GitHub](https://github.com)       | Gratis |
| [GitLab](https://gitlab.com)       | Gratis |
| [Bitbucket](https://bitbucket.org) | Gratis |

## Cliente de Interfaz de Usuario (GUI)

¿El terminal no es lo tuyo? Usa uno de los siguientes clientes.

| Cliente                                     | Sistema Operativo | Precio    |
| ------------------------------------------- | ----------------- | --------- |
| [GitHub](https://desktop.github.com)        | macOS y Windows   | Gratis    |
| [Sourcetree](https://www.sourcetreeapp.com) | macOS y Windows   | Gratis    |
| [Tower](https://www.git-tower.com)          | macOS y Windows   | $69 a $99 |
