# testllavessh
Test llaves ssh
Para crear la clave se ha de seguir los siguientes pasos en terminal (en mac) o en cmd (en windows).

ssh-keygen -t rsa -C "your_email@youremail.com" (sustituir "your_email@youremail.com" por el email que se puso al crear la cuenta de github).

Esto devolverá lo siguiente:

Generating public/private rsa key pair. Enter file in which to save the key. C/Users/your_user_directory/.ssh/id_rsa) Hacemos click en enter porque queremos que guarde la clave en el directorio por defecto. Guardará la clave ssh en el directorio .ssh dentro de nuestra carpeta de usuario.

Ahora nos dirá: Enter passphrase (empty for no passphrase) No hay por qué indicar nada. Enter.

Y nos dirá que la volvamos a introducir o darle a enter si lo dejamos en blanco antes.

Esto devolverá algo así.

Your identification has been saved in /Users/your_user_directory/.ssh/id_rsa. Your public key has been saved in /Users/your_user_directory/.ssh/id_rsa.pub

Debemos copiar la clave ssh. Para ello debemos introducir en la terminal lo siguiente o seguir los pasos indicados en windows:

En Mac: pbcopy < ~/.ssh/id_rsa.pub

En Windows: dirigirse la gui de git (llamada Git Extensions), ir a Help (Ayuda), Show Key (Mostrar Clave) y entonces presionar Copy to Clipboard (Copiar al portapales) para copiar la clave ssh al portapeles

Situar la clave SSH en Github.

Se deberá dirigir a Github y hacer click en "Add another pubic key". Control+v (Cmd+v en mac) en la zona de "Key" para situar ahí nuestra clave ssh. Se pone cualquier título en "Title". Por ej: algo para reconocer el pc del que es esa clave (Ej: Macbook Pro de Jesús).

Comprobación

Para comprobar que todo se ha hecho correctamente se debe introducir lo siguiente en la línea de comandos (cmd en windows, terminal en mac)

ssh -T git@github.com

Lo cual devolverá algo así

The authenticity of host ´github.com (123.123.123.123) can't be established. RSa key fingerprint is....... Are you sure you want to continue connecting (yes/no)

No te preocupes, esto debe ser así. Escribe yes.

Y eso devolverá

Hi 'username'! You've succesfully authenticated, ....

Llegados a este punto nuestro pc ya será capaz de conectarse al servidor de github y poder realizar todo tipo de acciones.

Por último se configurará nuestra info.



