# SOCIAL OPLESK
### 🏴‍☠️ HACK-GROUP

<br/>

📚 docs [markdown 1](https://agea.github.io/tutorial.md/) | [markdown 2](https://docs.github.com/es/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax) | [archivos de salud](https://docs.github.com/es/communities/setting-up-your-project-for-healthy-contributions/creating-a-default-community-health-file)
---
📚 docs [comandos git](https://gist.github.com/dasdo/9ff71c5c0efa037441b6) | [conventional commit](https://www.conventionalcommits.org/en/v1.0.0/)
---

```diff
- NOTA HACER LAS PRÁCTICAS MEDIANTE LA CONSOLA DE VSCODE y GITHUB
```

```
Se tienen 4 alias (alfa, bravo, charlie, delta), cada alia representa un integrante del equipo, 
si tu equipo tiene un integrante extra se llamara (echo) el procedimiento a realizar es el siguiente,
se necesita crear un circulo hábil en el manejo del pull request y manejo de array, para tal fin. 

Los integrantes deben definir la asignación de los alias del circuito
El circuito inicia con el usuario alfa
```
```diff
* Tienen que crear 4 repositorios y 1 repositorio extra, solo si tienen a echo en el equipo.
* El usuario a cargo del circuito según el turno del alias, aceptara las solicitudes de pull request del equipo
* Definir un contenido en el README.md con la siguiente estrucutra:
  * (titulo con el alias del encargado del repo / tabla de integrantes donde se refleje el nombre, ubicación de cada integrante) 
  * (si deseas anexar más info al README.md, tienes la libertad de expresar tus ideas)
* Copie el fragmento de texto que esta contenido en el sector PULL_REQUEST_TEMPLATE en el archivo PULL_REQUEST_TEMPLATE.md
```
<br/>

|Hacks | Details | 
|----------|---------|
| H-1      | Hacks |
| H-2      | Close Pull Request |
| H-3      | Code Review | 

<br/> 

---

### WORKFLOW

```mermaid
sequenceDiagram
    participant feature
    participant develop
    participant main
    feature->>develop: envia feature/foo a la rama develop
    develop->>main: los features en develop a la rama main
```

---

PULL_REQUEST_TEMPLATE
# Tipo de usuario
- [ ] Alfa
- [ ] Bravo 
- [ ] Charlie
- [ ] Delta
- [ ] Echo

# Tecnología
- [ ] HTML 
- [ ] Json 
- [ ] Archivo plano (.txt) 
- [ ] Javascript 
- [ ] Markdown / .md

# Seleccione el tipo de actividad
- [ ] Feature
- [ ] Changes
- [ ] Hotfix
- [ ] Refactor
- [ ] Performance
- [ ] Testing

---

|Alias  | 
|----------------------------------------------------------------------------------------------------
| foo, baz, charlie, qux, delta, quux, echo, corge, grault, garply, waldo, fred, plugh, xyzzy, thud, foobar |

<br/> 

---

#TIPS
```
    Los integrantes del proyecto deben hacer una actualización de su sucursal(repositorio) local
    git remote add upstream url_del_repositorio_foo
    git fetch upstream
    git switch main
    git merge upstream/main
 
    NOTA: Cuando el encargado del repositorio este modo "code review" en el ambiente de main-test(rama local)
    seguir los pasos de forma estricta con 2 opcione tú ejecutas la de tú preferencia

    opcion #1
    git fetch origin pull/id_del_pull_request/head:nombre-de-rama
    git switch main-test
    git merge nombreDelUsuario/nombre-de-rama --no-commit
    git switch main  

    opcion #2
    git fetch origin pull/id_del_pull_request/head:nombreDelUsuario/nombre-de-la-feature-NÚMERO-DE-PR
    git switch main-test
    git merge nombreDelUsuario/nombre-de-la-feature-NÚMERO-DE-PR --no-commit
    git switch main  
    
    Conectar tú repositorio local, con el repositorio base
    git remote add upstream url_del_repositorio_base.git
    
    Si la escuadra quiere recibir los últimos cambios del repositorio base, realizar lo siguiente:
    git fetch upstream
    git merge upstream/main
```
---

## 🏆 H-1

#### 👽 Usuario (Hacks)
```sh
 1. Deben crear 1 repositorio principal por cada ciclo "hg-2-foo" foo es el nombre del usuario asignado, dentro del equipo
    de alias (alfa, bravo, charlie, delta, echo) como administrador del repositorio en ese momento del ciclo, más
    los archivos de README.md.
 
 2. (Foo) crea la rama develop y anexa un archivo PULL_REQUEST_TEMPLATE.md dentro del repositorio /docs,
    luego hacer merge con main
    
 3. (Foo) debe hacer una feature donde va a detallar el CODE_OF_CONDUCT.md tiene que estar en el mismo directorio
    de /docs ahora como debes crear el CODE_OF_CONDUCT.md acá tienes una dirección de ejemplo:
    https://github.com/auth0/open-source-template/blob/master/CODE-OF-CONDUCT.md

 4. (Foo) cuando el CODE_OF_CONDUCT.md este listo, tienes que integrar la feature a la rama develop y luego
    anexar los cambios al ambiente principal, que es la rama main
 
 5. Cada usuario debe enviar 1 directorio con su nombre de alias con 2 archivos de extensión ".html / .txt"
    el directorio y los archivos según su alias ejemplo:

    📁alfa
      |---- alfa.html
      |---- config-alfa.txt
      |---- data-alfa.json


    * ejemplo del envio de RAMAS
    feature/alfa
    feature/alfa-hack
    feature/alfa-task-number
    feature/feature-alfa
    feature/feature-alfa-task-number
```     
 
---
## 🏆 H-2
#### 👽 (Close Pull Request)
```sh
6. Ahora cada participante envia una feature, con 1 archivo de extensión ".json" con el nombre de su alias,
   esta feature la deben enviar directamente al ambiente principal(main), ahora el administrador del repositorio
   anula la solicitud pull request

   📁alfa
      |---- data-alfa.json
 
7  Luego cada participantes debe enviar la solicitud del PR del archivo ".json" al ambiente
   de desarrollo(develop) y el administrador integrar el PR al ambiente de desarrollo(develop)
```   

---

## 🏆 H-3
#### 👽 (Code Review)

```sh
8. Desde Oplesk enviamos (Felicitaciones a todos los integrantes de la escuadra), llegar a este punto, requiere de un 
    gran esfuerzo, compromiso y sobre todo, de un excelente trabajo de equipo.
 
9. Por último, la escuadra necesita crear un archivo con su alias "alias-about.html" en el archivo escribir:
    <h1>Hola soy tu-alias<>
   seguramente el vscode dará una alerta de error, aunque la intención es enviar un código con defecto  
 
10. Ejemplo el usuario (Foo) debe descargar cada solicitud de PR con el archivo de "alias-about.html"
     Busca el número de la Pull Request en GitHub y ve a la terminal, para descargar la feature de la
     solicitud del pull request y realizar el code review, en una rama de prueba main-test.

     En la sección tips en la parte superior de tópico aparece 2 opciones de hacer esta operación
 
     git fetch origin pull/id_del_pull_request/head:nombre-de-la-rama-pr
     git switch main-test
     git merge nombre-de-la-rama-pr --no-commit
     git switch main
 
11. El usuario (Foo) declina el PR, con el comentario que el código le falta el cierre de la etiqueta "h1"
 
12. Los integrantes deben enviar la tarea devuelta con el cierre del </h1> como recomendación
    enviar su alias de usuario.
 
13. Ahora el usuario (Foo) debe hacer los mismos pasos por cada usuario, Si la feature enviada se encuentra solucionada aceptar el PR.
    hacia la rama develop y luego enviar los cambios al ambiente de producción(main)

    consejo elimina las ramas nombre-de-la-rama-pr antes de realizar el "code review
    ejemplo:
 
    git branch -D  nombre-de-la-rama-pr

```
