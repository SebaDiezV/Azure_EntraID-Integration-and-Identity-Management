# Proyecto 4 : Entra ID Integration and Identity Management

## Temas Tratados
Entra ID, User and Group Management, App Registration, Conditional Access, MFA

## Resumen
Este proyecto demuestra cómo integrar aplicaciones con Entra ID, administrar usuarios y grupos, configurar políticas de acceso condicional, habilitar MFA y monitorear la actividad de autenticación.

## Escenario
Una empresa desea integrar su aplicación web con Entra ID para autenticación, administrar permisos de usuarios y grupos, aplicar políticas de acceso condicional y habilitar la autenticación multifactor (MFA) para mayor seguridad

>**Nota**: Para este proyecto necesitas contar con la licencia **Azure AD Premium P1**

## Tarea 1: Crear Usuarios y Grupos en Entra ID

1. En el **Portal de Azure** ingresa a **Microsoft Entra ID**
<img width="254" alt="01" src="https://github.com/user-attachments/assets/d936d2a1-9f03-4e9f-baad-5a32c20e63fc" />

2. En **Administrar**, ingresa a **Usuarios**
<img width="159" alt="02" src="https://github.com/user-attachments/assets/6c536698-8e61-479b-861d-ce8e0fb56f83" />

3. En **Todos los usuarios**, selecciona **+ Nuevo usuarios** > **Crear un nuevo usuario**
<img width="304" alt="03" src="https://github.com/user-attachments/assets/d650cf26-5985-42d0-afe1-44cc1b9f7df5" />

4. Crea algunos usuarios con diferentes roles (por ejemplo, administrador, desarrollador, lector)
<img width="370" alt="04" src="https://github.com/user-attachments/assets/12cf2cda-b3c6-4701-8b83-bc77a0aa0803" />

5. Vuelve a la página principal de **Entra ID**, selecciona **Administrar** > **Grupos** > **Nuevo grupo**
<img width="158" alt="06" src="https://github.com/user-attachments/assets/f796998e-ec8a-4aa8-b6e9-9dbfbae7ffff" />
<img width="241" alt="07" src="https://github.com/user-attachments/assets/bccd9a8e-8660-4125-9486-a8c1c591a573" />

6. Crea un nuevo grupo y asigna a los usuarios anteriormente creados
<img width="394" alt="08" src="https://github.com/user-attachments/assets/de9f3e0a-a59c-4f15-beb6-093b54150f16" />

## Tarea 2: Registrar una aplicación en Entra ID

1. En **Entra ID**, selecciona **Administrar** > **Registro de aplicaciones** > **+ Nuevo Registro**
<img width="386" alt="09" src="https://github.com/user-attachments/assets/d7a145b7-0667-467c-8ca1-37ae3dc8552f" />

2. Ingresa un nombre, los tipos de cuenta admitidos y una URI de redireccionamiento (por ejemplo, para una aplicación web) > Registrar
<img width="618" alt="10" src="https://github.com/user-attachments/assets/78fbe344-271e-477c-9b76-d02358bdd6c8" />

3. Vuelve a **Registro de aplicaciones** y selecciona la aplicación creada
<img width="475" alt="11-2" src="https://github.com/user-attachments/assets/d9ffac60-ced1-43cb-9ace-75e2fe086e33" />

4. Selecciona **Administrar** > **Permisos de API**, verifica que la API de **Microsoft Graph** tenga permisos
<img width="781" alt="13" src="https://github.com/user-attachments/assets/05c8aaa6-8ecd-432e-870b-336069e50a82" />

5. Selecciona **Administrar** > **Certificados y secretos** > **+ Nuevo secreto de cliente**, agrega una descripción y tiempo de expiración > Agregar
<img width="740" alt="14" src="https://github.com/user-attachments/assets/c95f4f11-0885-4220-802c-d082739abba7" />

<img width="339" alt="15" src="https://github.com/user-attachments/assets/fa4a6f56-2372-44cd-9eec-566edf85d2b3" />

## Tarea 3: Asignar Usuarios y Grupos a la aplicación

1. En **Entra ID** dirígete a **Administrar** > **Aplicaciones empresariales**, selecciona la aplicación creada
<img width="157" alt="16" src="https://github.com/user-attachments/assets/6c05a3c7-0c3a-4c6e-9d56-6b5025461227" />
<img width="301" alt="17" src="https://github.com/user-attachments/assets/a8c40fea-3ac1-4c6a-84d8-503eed4e8767" />

2. Selecciona **Asignar usuarios y grupos** > **+ Agregar usuario y grupo**
<img width="391" alt="18" src="https://github.com/user-attachments/assets/bf019670-2c44-4fa5-ae86-eef601885815" />
<img width="289" alt="19" src="https://github.com/user-attachments/assets/14eda7ad-0567-42ed-a482-22c018c36e71" />

3. Busca el grupo creado con anterioridad, Seleccionar > Asignar
<img width="958" alt="20" src="https://github.com/user-attachments/assets/e1e14455-531a-4de9-8cc9-8bf425a20030" />

4. verifica que el grupo quedó asignado de manera correcta
<img width="575" alt="21" src="https://github.com/user-attachments/assets/2dc40dde-5cb8-4e4b-a521-dbc4c0fffdef" />

## Tarea 4: Configurar Acceso Condicional

1. En **Entra ID**, dirígete a **Administrar** > **Seguridad**
<img width="153" alt="22" src="https://github.com/user-attachments/assets/23672e5f-41b6-4b06-a234-ac27ccb94043" />

2. Dirígete a **Proteger** > **Acceso condicional** y selecciona **+ Crear nueva directiva**
<img width="270" alt="23" src="https://github.com/user-attachments/assets/e5afdd10-718d-4aae-9315-3c57d56aaff5" />

3. A continuación, se creará una directiva que requiera MFA para acceder a la aplicación. Agrega un nombre a la nueva directiva, En **Usuarios** selecciona el grupo de usuarios creado anteriormente
<img width="390" alt="24" src="https://github.com/user-attachments/assets/27569024-8a5d-43fa-ae06-621d20bdd876" />

4. En **Recursos de destino** agregar la aplicación creada para que sea el objetivo de la directiva
<img width="400" alt="25" src="https://github.com/user-attachments/assets/a5371741-0499-4487-ba8f-df8e8a40bc21" />

5. En **Condiciones** agrega las condiciones de cumplimiento necesarias, en este caso, configuré las **Plataformas de dispositivo** admitidas para conectar a la aplicación
<img width="952" alt="26" src="https://github.com/user-attachments/assets/10a6a791-d51d-478f-aaf6-dabf03754464" />

6.  En **Conceder**, selecciona **Requerir autenticación multifactor** para **Conceder acceso**
<img width="954" alt="27" src="https://github.com/user-attachments/assets/c0240696-410c-45dd-8d5f-0c8c6ab72cf7" />

7. En **Habilitar directiva** Seleccionar **Activado** > Crear
<img width="160" alt="28" src="https://github.com/user-attachments/assets/93f34cde-5a61-4eb6-8f1a-a53d1b4bf39e" />

>**Nota**: Si se activó recientemente la licencia **Azure AD Premium P1**, se deben **deshabilitar los valores predeterminados de seguridad** antes de crear una nueva directiva
>
> <img width="725" alt="29" src="https://github.com/user-attachments/assets/b67e168b-c212-4d32-a26c-ec000aedf747" />
> <img width="255" alt="30" src="https://github.com/user-attachments/assets/7e329b3e-f448-4f33-9f7c-9b2e6123eaae" />

## Tarea 5: Habilitar Autenticación Multifactor (MFA)

1. En **Entra ID**, selecciona **Usuarios** > **MFA por usuario**
<img width="789" alt="31" src="https://github.com/user-attachments/assets/9a1d631f-b197-4371-bd10-5b3221acc43d" />

2. Selecciona a algún usuario y selecciona la opción **Habilitar MFA**
<img width="168" alt="32" src="https://github.com/user-attachments/assets/52ec4592-2802-4fb4-b87b-694bbc26ed49" />

3. En un navegador incognito ingresa a **portal.office.com** con las credenciales del usuario, se solicitará la configuración de MFA 
<img width="430" alt="33" src="https://github.com/user-attachments/assets/49f48bb5-e97d-46cc-85b9-5e0bddcac671" />

## Tarea 6: Monitorear la actividad de inicio de sesión

1. En **Entra ID**, selecciona **Supervisión** > **Registros de inicio de sesión**, Revisa los registros de inicio de sesión para verificar los intentos de autenticación exitosos y fallidos

<img width="867" alt="34" src="https://github.com/user-attachments/assets/b96dc0d5-8e84-4e53-8765-f202517f1bb7" />


