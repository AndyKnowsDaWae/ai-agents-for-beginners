<!--
CO_OP_TRANSLATOR_METADATA:
{
  "original_hash": "9b03446058b4eed46928ae5e46325ea0",
  "translation_date": "2025-10-02T19:13:39+00:00",
  "source_file": "00-course-setup/README.md",
  "language_code": "es"
}
-->
# Configuración del Curso

## Introducción

Esta lección cubrirá cómo ejecutar los ejemplos de código de este curso.

## Únete a Otros Estudiantes y Obtén Ayuda

Antes de comenzar a clonar tu repositorio, únete al [canal de Discord AI Agents For Beginners](https://aka.ms/ai-agents/discord) para obtener ayuda con la configuración, resolver cualquier duda sobre el curso o conectarte con otros estudiantes.

## Clona o Haz un Fork de este Repositorio

Para comenzar, por favor clona o haz un fork del repositorio de GitHub. Esto creará tu propia versión del material del curso para que puedas ejecutar, probar y ajustar el código.

Esto se puede hacer haciendo clic en el enlace para <a href="https://github.com/microsoft/ai-agents-for-beginners/fork" target="_blank">hacer un fork del repositorio</a>.

Ahora deberías tener tu propia versión del curso en el siguiente enlace:

![Repositorio Forkeado](../../../translated_images/forked-repo.33f27ca1901baa6a5e13ec3eb1f0ddd3a44d936d91cc8cfb19bfdb9688bd2c3d.es.png)

## Ejecutar el Código

Este curso ofrece una serie de Jupyter Notebooks que puedes ejecutar para obtener experiencia práctica construyendo Agentes de IA.

Los ejemplos de código utilizan:

**Requiere una cuenta de GitHub - Gratis**:

1) Framework Semantic Kernel Agent + GitHub Models Marketplace. Etiquetado como (semantic-kernel.ipynb)
2) Framework AutoGen + GitHub Models Marketplace. Etiquetado como (autogen.ipynb)

**Requiere una suscripción a Azure**:
3) Azure AI Foundry + Azure AI Agent Service. Etiquetado como (azureaiagent.ipynb)

Te animamos a probar los tres tipos de ejemplos para ver cuál funciona mejor para ti.

La opción que elijas determinará los pasos de configuración que debes seguir a continuación:

## Requisitos

- Python 3.12+
  - **NOTA**: Si no tienes Python 3.12 instalado, asegúrate de instalarlo. Luego crea tu entorno virtual usando python3.12 para garantizar que se instalen las versiones correctas desde el archivo requirements.txt.
  
    >Ejemplo

    Crear directorio de entorno virtual de Python:

    ``` bash
    python3 -m venv venv
    ```

    Luego activa el entorno virtual para:

    macOS y Linux

    ```bash
    source venv/bin/activate
    ```
  
    Windows

    ```bash
    venv\Scripts\activate
    ```

- Una cuenta de GitHub - Para acceder al GitHub Models Marketplace
- Suscripción a Azure - Para acceder a Azure AI Foundry
- Cuenta de Azure AI Foundry - Para acceder al Azure AI Agent Service

Hemos incluido un archivo `requirements.txt` en la raíz de este repositorio que contiene todos los paquetes de Python necesarios para ejecutar los ejemplos de código.

Puedes instalarlos ejecutando el siguiente comando en tu terminal en la raíz del repositorio:

```bash
pip install -r requirements.txt
```

Recomendamos crear un entorno virtual de Python para evitar conflictos y problemas.

## Configuración de VSCode
Asegúrate de estar utilizando la versión correcta de Python en VSCode.

![image](https://github.com/user-attachments/assets/a85e776c-2edb-4331-ae5b-6bfdfb98ee0e)

## Configuración para Ejemplos usando Modelos de GitHub 

### Paso 1: Obtén tu Token de Acceso Personal (PAT) de GitHub

Este curso utiliza el GitHub Models Marketplace, que proporciona acceso gratuito a Modelos de Lenguaje Extenso (LLMs) que usarás para construir Agentes de IA.

Para usar los modelos de GitHub, necesitarás crear un [Token de Acceso Personal de GitHub](https://docs.github.com/en/authentication/keeping-your-account-and-data-secure/managing-your-personal-access-tokens).

Esto se puede hacer yendo a la <a href="https://github.com/settings/personal-access-tokens" target="_blank">configuración de Tokens de Acceso Personal</a> en tu cuenta de GitHub.

Por favor, sigue el [Principio de Mínimos Privilegios](https://docs.github.com/en/get-started/learning-to-code/storing-your-secrets-safely) al crear tu token. Esto significa que solo debes otorgar al token los permisos necesarios para ejecutar los ejemplos de código de este curso.

1. Selecciona la opción `Fine-grained tokens` en el lado izquierdo de tu pantalla navegando a **Developer settings**.
   ![](../../../translated_images/profile_developer_settings.410a859fe749c755c859d414294c5908e307222b2c61819c3203bbeed4470e25.es.png)

    Luego selecciona `Generate new token`.

    ![Generar Token](../../../translated_images/fga_new_token.1c1a234afe202ab37483944a291ee80c1868e1e78082fd6bd4180fea5d5a15b4.es.png)

2. Ingresa un nombre descriptivo para tu token que refleje su propósito, facilitando su identificación más adelante.

    🔐 Recomendación de Duración del Token

    Duración recomendada: 30 días  
    Para una postura más segura, puedes optar por un período más corto, como 7 días 🛡️  
    Es una excelente manera de establecer un objetivo personal y completar el curso mientras tu impulso de aprendizaje está alto 🚀.

    ![Nombre y Expiración del Token](../../../translated_images/token-name-expiry-date.a095fb0de63868640a4c82d6b1bbc92b482930a663917a5983a3c7cd1ef86b77.es.png)

3. Limita el alcance del token a tu fork de este repositorio.

    ![Limitar alcance al repositorio forkeado](../../../translated_images/token_repository_limit.924ade5e11d9d8bb6cd21293987e4579dea860e2ba66d607fb46e49524d53644.es.png)

4. Restringe los permisos del token: En **Permissions**, haz clic en la pestaña **Account** y luego en el botón "+ Add permissions". Aparecerá un menú desplegable. Busca **Models** y marca la casilla correspondiente.
    ![Agregar Permiso de Modelos](../../../translated_images/add_models_permissions.c0c44ed8b40fc143dc87792da9097d715b7de938354e8f771d65416ecc7816b8.es.png)

5. Verifica los permisos requeridos antes de generar el token.  
    ![Verificar Permisos](../../../translated_images/verify_permissions.06bd9e43987a8b219f171bbcf519e45ababae35b844f5e9757e10afcb619b936.es.png)

6. Antes de generar el token, asegúrate de estar listo para almacenarlo en un lugar seguro como un gestor de contraseñas, ya que no se mostrará nuevamente después de crearlo.  
    ![Almacenar Token de Forma Segura](../../../translated_images/store_token_securely.08ee2274c6ad6caf3482f1cd1bad7ca3fdca1ce737bc485bfa6499c84297c789.es.png)

Copia tu nuevo token que acabas de crear. Ahora lo agregarás a tu archivo `.env` incluido en este curso.

### Paso 2: Crea tu Archivo `.env`

Para crear tu archivo `.env`, ejecuta el siguiente comando en tu terminal.

```bash
cp .env.example .env
```

Esto copiará el archivo de ejemplo y creará un `.env` en tu directorio donde completarás los valores de las variables de entorno.

Con tu token copiado, abre el archivo `.env` en tu editor de texto favorito y pega tu token en el campo `GITHUB_TOKEN`.  
![Campo de Token de GitHub](../../../translated_images/github_token_field.20491ed3224b5f4ab24d10ced7a68c4aba2948fe8999cfc8675edaa16f5e5681.es.png)

Ahora deberías poder ejecutar los ejemplos de código de este curso.

## Configuración para Ejemplos usando Azure AI Foundry y Azure AI Agent Service

### Paso 1: Obtén tu Endpoint de Proyecto de Azure

Sigue los pasos para crear un hub y proyecto en Azure AI Foundry que se encuentran aquí: [Descripción general de recursos del hub](https://learn.microsoft.com/en-us/azure/ai-foundry/concepts/ai-resources)

Una vez que hayas creado tu proyecto, necesitarás obtener la cadena de conexión para tu proyecto.

Esto se puede hacer yendo a la página **Overview** de tu proyecto en el portal de Azure AI Foundry.

![Cadena de Conexión del Proyecto](../../../translated_images/project-endpoint.8cf04c9975bbfbf18f6447a599550edb052e52264fb7124d04a12e6175e330a5.es.png)

### Paso 2: Crea tu Archivo `.env`

Para crear tu archivo `.env`, ejecuta el siguiente comando en tu terminal.

```bash
cp .env.example .env
```

Esto copiará el archivo de ejemplo y creará un `.env` en tu directorio donde completarás los valores de las variables de entorno.

Con tu token copiado, abre el archivo `.env` en tu editor de texto favorito y pega tu token en el campo `PROJECT_ENDPOINT`.

### Paso 3: Inicia sesión en Azure

Como práctica de seguridad, utilizaremos [autenticación sin claves](https://learn.microsoft.com/azure/developer/ai/keyless-connections?tabs=csharp%2Cazure-cli?WT.mc_id=academic-105485-koreyst) para autenticarte en Azure OpenAI con Microsoft Entra ID.

A continuación, abre un terminal y ejecuta `az login --use-device-code` para iniciar sesión en tu cuenta de Azure.

Una vez que hayas iniciado sesión, selecciona tu suscripción en el terminal.

## Variables de Entorno Adicionales - Azure Search y Azure OpenAI 

Para la lección de Agentic RAG - Lección 5 - hay ejemplos que utilizan Azure Search y Azure OpenAI.

Si deseas ejecutar estos ejemplos, necesitarás agregar las siguientes variables de entorno a tu archivo `.env`:

### Página de Descripción General (Proyecto)

- `AZURE_SUBSCRIPTION_ID` - Consulta **Project details** en la página **Overview** de tu proyecto.

- `AZURE_AI_PROJECT_NAME` - Mira la parte superior de la página **Overview** de tu proyecto.

- `AZURE_OPENAI_SERVICE` - Encuentra esto en la pestaña **Included capabilities** para **Azure OpenAI Service** en la página **Overview**.

### Centro de Gestión

- `AZURE_OPENAI_RESOURCE_GROUP` - Ve a **Project properties** en la página **Overview** del **Management Center**.

- `GLOBAL_LLM_SERVICE` - En **Connected resources**, encuentra el nombre de conexión de **Azure AI Services**. Si no está listado, consulta el **Azure portal** en tu grupo de recursos para el nombre del recurso de AI Services.

### Página de Modelos + Endpoints

- `AZURE_OPENAI_EMBEDDING_DEPLOYMENT_NAME` - Selecciona tu modelo de embedding (por ejemplo, `text-embedding-ada-002`) y toma nota del **Deployment name** de los detalles del modelo.

- `AZURE_OPENAI_CHAT_DEPLOYMENT_NAME` - Selecciona tu modelo de chat (por ejemplo, `gpt-4o-mini`) y toma nota del **Deployment name** de los detalles del modelo.

### Portal de Azure

- `AZURE_OPENAI_ENDPOINT` - Busca **Azure AI services**, haz clic en él, luego ve a **Resource Management**, **Keys and Endpoint**, desplázate hacia abajo hasta "Azure OpenAI endpoints" y copia el que dice "Language APIs".

- `AZURE_OPENAI_API_KEY` - Desde la misma pantalla, copia KEY 1 o KEY 2.

- `AZURE_SEARCH_SERVICE_ENDPOINT` - Encuentra tu recurso de **Azure AI Search**, haz clic en él y consulta **Overview**.

- `AZURE_SEARCH_API_KEY` - Luego ve a **Settings** y luego a **Keys** para copiar la clave de administrador primaria o secundaria.

### Página Externa

- `AZURE_OPENAI_API_VERSION` - Visita la página [Ciclo de vida de la versión de API](https://learn.microsoft.com/en-us/azure/ai-services/openai/api-version-deprecation#latest-ga-api-release) bajo **Última versión GA de API**.

### Configuración de autenticación sin claves

En lugar de codificar tus credenciales, utilizaremos una conexión sin claves con Azure OpenAI. Para hacerlo, importaremos `DefaultAzureCredential` y luego llamaremos a la función `DefaultAzureCredential` para obtener la credencial.

```python
from azure.identity import DefaultAzureCredential, InteractiveBrowserCredential
```

## ¿Atascado en algún lugar?

Si tienes algún problema ejecutando esta configuración, únete a nuestro <a href="https://discord.gg/kzRShWzttr" target="_blank">Discord de la Comunidad Azure AI</a> o <a href="https://github.com/microsoft/ai-agents-for-beginners/issues?WT.mc_id=academic-105485-koreyst" target="_blank">crea un issue</a>.

## Próxima Lección

Ahora estás listo para ejecutar el código de este curso. ¡Feliz aprendizaje sobre el mundo de los Agentes de IA!

[Introducción a los Agentes de IA y Casos de Uso de Agentes](../01-intro-to-ai-agents/README.md)

---

**Descargo de responsabilidad**:  
Este documento ha sido traducido utilizando el servicio de traducción automática [Co-op Translator](https://github.com/Azure/co-op-translator). Si bien nos esforzamos por lograr precisión, tenga en cuenta que las traducciones automáticas pueden contener errores o imprecisiones. El documento original en su idioma nativo debe considerarse como la fuente autorizada. Para información crítica, se recomienda una traducción profesional realizada por humanos. No nos hacemos responsables de malentendidos o interpretaciones erróneas que puedan surgir del uso de esta traducción.