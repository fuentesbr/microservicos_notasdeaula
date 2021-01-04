# Gitflow

## Gitflow

Gitflow é um processo que visa utilizar o git como ferramenta para gerenciar a criação de novas features,
correções de bugs e releases.

### Importância da padronização do processo de desenvolvimento

(forma inadequada)
* git checkout -b formulario_de_registro
* git checkout -b bug_01
* git push origin master

(forma correta)
* git checkout -b feature/registro
* git ckeckout -b hotfix/registro
* git push origin develop
* git ckeckout master && git merge develop

Conceito - Flow

* Padrão
* Legibilidade
* Processo

### Como funciona o Gitflow

    /* MASTER */                                        /* DEVELOP */

    - Regra de Ouro Nunca comitar direto no master!         /** FEATURES **/
                                                            /** RELEASES **/
                                                            /** HOTFIX   **/


### Features

    /* Develop */ --> /** Feature **/

git checkout develop
git ckeckout -b feature/register

    /* Develop */ <-- /** Feature **/

git ckeckout develop
git merge feature/register

### Releases

    /* Develop */ --> /** Release **/ --> /** Master **/

git checkout develop
git checkout -b release/1.0.0
git checkout master
git merge release/1.0.0

### Hotfix

    /* Master */
                    <-- /** Hotfix **/
    /* Develop */

git checkout master
git merge hotfix/recurso
git checkout develop
git merge hotfix/recurso
git branch -D hotfix/recurso

### Extensão Gitflow

Gitflow possui uma extensão para facilitar todo o processo, porém a utilização da mesma
é TOTALMENTE opcional.


Para iniciar um projeto usando a extensão

git flow init

git flow feature start feature/register
git flow feature finish feature/register

git flow release start 1.0.0
git flow release finish '1.0.0'

git flow hotfix start hotfix/recurso
git flow hotfix finish hotfix/recurso

## Gitflow na prática

Prefixo support - para manter versões mais antigas

## Gitflow com Pull Requests

### Pull Request

Sobe algo que está em outro repositório/branch e queremos dar uma pull request, para solicitar um merge em um repositório.

## Trabalhando com releases

Toda vez que fizer um release, tanto developer quanto master devem estar no mesmo tag