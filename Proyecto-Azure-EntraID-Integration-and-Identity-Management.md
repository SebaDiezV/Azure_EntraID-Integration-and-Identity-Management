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

5. Selecciona **Administrar** > **Certificados y secretos** > **+ Nuevo secreto de cliente**, agrega una decripción y tiempo de expiración > Agregar
<img width="740" alt="14" src="https://github.com/user-attachments/assets/c95f4f11-0885-4220-802c-d082739abba7" />

<img width="339" alt="15" src="https://github.com/user-attachments/assets/fa4a6f56-2372-44cd-9eec-566edf85d2b3" />

## Tarea 3: Asignar Usuarios y Grupos a la aplicación

1. En **Entra ID** dirigete a **Asministrar** > **Aplicaciones empresariales**, selecciona la aplicación creada
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

**PLACEHOLDER**
