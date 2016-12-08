# Plantilla HTML5

## Descripcion

Este proyecto contiene una plantilla de HTML5 con CDN de Bootsrap v.3.3.7 y jQuery 1.12.4.

## Proposito

Poder utilizar la plantilla en nuevos proyectos que necesiten de Bootsrap y jQuery

### Tutorial para usar comandos git creando un nuevo proyecto
    
    git init // crea o inicia git dentro de la carpeta del nuevo proyecto

    git remote add origin <servidor> // conectar el repositorio local a un repositorio remoto

    git add <nombre del archivo> // agregar un archivo al repositorio
        git add . // agregar todos los archivos al repositorio
        git commit -m "comentario" // crear comentario a los cambios realizados, hace incluir los
                                        archivos en el HEAD, pero no en el repositorio remoto
    git push origin master // enviar los cambios al repositorio remoto

    git clone username@host:/path/to/repository // crear una copia local del repositorio remoto

    git status // verificar el estado del repositorio local


### Tutorial para Generar una nueva clave SSH
    
   1. Abra la Terminal.

   2. Pegue el texto que aparece a continuación, sustituyéndolo por su dirección de 
        correo electrónico del GitHub.

        ssh-keygen -t rsa -b 4096 -C "your_email@example.com"


    Esto crea una nueva clave ssh, utilizando el correo electrónico proporcionado como una etiqueta.
    
   3. Cuando se le solicite "Introduzca un archivo en el que guardara la clave" y pulse Intro. Esto acepta la ubicación de archivo predeterminada.
        
        Enter a file in which to save the key (/Users/you/.ssh/id_rsa): [Press enter]
        
   4. En el indicador, escriba una contraseña segura.
   
        Enter passphrase (empty for no passphrase): [Type a passphrase]
        Enter same passphrase again: [Type passphrase again]

### Tutorial para agregar la clave SSH generada al agente ssh
   1. Agregue su clave SSH al agente ssh. Si utilizó una clave SSH existente en lugar de generar una nueva clave SSH, deberá reemplazar id_rsa en el comando por el nombre de su archivo de clave privada existente. Por ejemplo: id_rsa_mi_nombre
        
        $ ssh-add ~/.ssh/id_rsa
        
   2. Puede comprobar la clave guardada
    
        $ ssh-add -l

#### Modificar la configuración ssh
    
    $ cd ~/.ssh/
    $ touch config
    $ subl -a config
    
   . Despues agregar:
   
    #activehacker account
    Host github.com-activehacker
        HostName github.com
        User git
        IdentityFile ~/.ssh/id_rsa_activehacker
        IdentitiesOnly yes


### Agregar una nueva clave SSH a tu cuenta de GitHub

   1. Copie la clave SSH en su portapapeles.
   
   Si su archivo de clave SSH tiene un nombre diferente al código de ejemplo, modifique el nombre de archivo para que coincida con su configuración actual. Al copiar la clave, no añada ninguna nueva línea o espacio en blanco.
   
    $ pbcopy < ~/.ssh/id_rsa.pub
    # Copia el contenido del archivo id_rsa.pub en el portapapeles
    
   2. En la esquina superior derecha de cualquier página, haz clic en tu foto de perfil y, a continuación, haz clic en **Settings**.

   3. En la barra lateral Configuración de usuario, haga clic en **SSH and GPG keys**.
   
   4. Haga Clic en **New SSH key** o **Add SSH key**.
   
   5. En el campo "Título", agregue una etiqueta descriptiva para la nueva clave. Por ejemplo, si está utilizando una Mac personal, puede llamar a esta clave "Personal MacBook Air".
   
   6. Pegue la clave en el campo "Clave".
   
   7. Si se le solicita, confirme su contraseña de GitHub.
   
   
##### Fuente de los tutoriales:
   
   1. Tutorial para Generar una nueva clave SSH y agregarla al agente ssh en [este](https://help.github.com/articles/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent/) enlace.
   2. Agregar una nueva clave SSH a tu cuenta de GitHub en [este](https://help.github.com/articles/adding-a-new-ssh-key-to-your-github-account/) enlace.
   3. Tutorial para configurar varias claves SSH para diferentes cuentas github en [este](https://gist.github.com/jexchan/2351996) enlace.

   Si no funcionan los enlaces dejo los enlaces completos aqui abajo:

    https://help.github.com/articles/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent/
    https://help.github.com/articles/adding-a-new-ssh-key-to-your-github-account/
    https://gist.github.com/jexchan/2351996