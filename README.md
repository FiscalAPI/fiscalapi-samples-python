# FiscalAPI SDK para Python

[![PyPI version](https://badge.fury.io/py/fiscalapi.svg)](https://badge.fury.io/py/fiscalapi)
[![License: MPL-2.0](https://img.shields.io/badge/License-MPL_2.0-blue.svg)](https://github.com/FiscalAPI/fiscalapi-python/blob/main/LICENSE.txt)

Ejemplos del SDK de FiscalAPI para python, la API de facturación CFDI y otros servicios fiscales en México. Simplifica la integración con los servicios de facturación electrónica, eliminando las complejidades del de la autoridad tributaria (SAT) y facilitando la generación de facturas, notas de crédito y complementos de pago, nómina, carta porte, etc.

La aplicación consiste en un único script `app.py` que contiene diversos ejemplos comentados para demostrar las diferentes funcionalidades de la API.

## 🚀 Características

El SDK de FiscalAPI para Python ofrece una amplia gama de funcionalidades para la facturación electrónica en México:

### Facturación CFDI 4.0
- Timbrado de facturas de ingreso
- Timbrado de notas de crédito (facturas de egreso)
- Timbrado de complementos de pago
- Consulta del estatus de facturas en el SAT
- Cancelación de facturas
- Generación de archivos PDF de las facturas
- Personalización de logos y colores en los PDF
- Envío de facturas por correo electrónico
- Descarga de archivos XML

### Gestión de personas
- Administración de personas (emisores, receptores, clientes, usuarios, etc)
- Gestión de certificados CSD (subir archivos .cer y .key a fiscalapi)
- Configuración de datos fiscales (RFC, domicilio fiscal, régimen fiscal)

### Gestion de productos/servicios
- Gestión de productos y servicios
- Administración de impuestos aplicables (IVA, ISR, IEPS)

### Consulta de catalogos SAT
- Consulta en catálogos oficiales del SAT
- Búsqueda de información en catálogos del SAT

### Integración y configuración
- Configuración de ambiente (pruebas o producción)
- Gestión de credenciales y tokens de autenticación
- Respuestas en formato estructurado para fácil procesamiento


## Requisitos previos de este ejemplo:

- Python 3.8 o superior
- pip (gestor de paquetes de Python)
- Opcional: Visual Studio Code para una mejor experiencia de desarrollo

## Configuración del entorno

### 1. Clonar el repositorio

```bash
git clone https://github.com/FiscalAPI/fiscalapi-samples-python.git
cd fiscalapi-samples-python
```

### 2. Crear un entorno virtual

Es recomendable utilizar un entorno virtual para mantener las dependencias del proyecto aisladas.

#### En Windows:

```bash
python -m venv .venv
.venv\Scripts\activate
```

#### En macOS/Linux:

```bash
python3 -m venv .venv
source .venv/bin/activate
```

Una vez activado el entorno virtual, verás el nombre del entorno en tu terminal.

### 3. Instalar dependencias

Instala la biblioteca FiscalAPI:

```bash
pip install fiscalapi
```

## Configuración de credenciales

Antes de ejecutar los ejemplos, es necesario configurar tus credenciales de FiscalAPI. Para obtener tus credenciales, puedes consultar la [Obtener credenciales de prueba](https://docs.fiscalapi.com/credentials-info).

Edita el archivo `app.py` y ubica la sección de configuración:

```python
settings = FiscalApiSettings(
    api_url="https://test.fiscalapi.com",  # https://live.fiscalapi.com (producción)
    api_key="tu_api_key",  # Reemplaza con tu API Key
    tenant="tu_tenant_key"  # Reemplaza con tu Tenant Key
)
```

Reemplaza `tu_api_key` y `tu_tenant_key` con tus [credenciales](https://docs.fiscalapi.com/credentials-info) obtenidas del portal de FiscalAPI.

## Ejecutar los ejemplos

El archivo `app.py` contiene muchos ejemplos comentados. Para ejecutar un ejemplo específico:

1. Abre el archivo `app.py` en tu editor de código
2. Descomenta el ejemplo que desees probar.
3. Guarda el archivo

### Opciones para ejecutar el script:

#### Opción 1: Desde la línea de comandos

```bash
python app.py
```

#### Opción 2: Desde Visual Studio Code

1. Abre el archivo `app.py` en Visual Studio Code
2. Haz clic en el botón "Run Python File" (▶️) ubicado en la esquina superior derecha del editor
3. Verás la salida en la terminal integrada de VS Code


## Solución de problemas

Si encuentras errores relacionados con la instalación de paquetes o la ejecución del script:

1. Verifica que estás utilizando la versión correcta de Python (3.8+)
2. Asegúrate de que el entorno virtual esté activado
3. Asegurate de usar la ultima versón el paquete: `pip install --upgrade fiscalapi`
4. Verifica que tus credenciales (API Key y Tenant Key) sean correctas
5. Revisa la documentación oficial de FiscalAPI para más información


## 🤝 Contribuir

1. Haz un fork del repositorio.
2. Crea una rama para tu feature: `git checkout -b feature/AmazingFeature`
3. Realiza commits de tus cambios: `git commit -m 'Add some AmazingFeature'`
4. Sube tu rama: `git push origin feature/AmazingFeature`
5. Abre un Pull Request en GitHub.

## 🐛 Reportar Problemas

1. Asegúrate de usar la última versión del SDK.
2. Verifica si el problema ya fue reportado.
3. Proporciona un ejemplo mínimo reproducible.
4. Incluye los mensajes de error completos.

## 📄 Licencia

Este proyecto está licenciado bajo la Licencia **MPL**. Consulta el archivo [LICENSE](LICENSE.txt) para más detalles.

## 🔗 Enlaces Útiles

- [Documentación Oficial](https://docs.fiscalapi.com)
- [Como obtener mis credenciales](https://docs.fiscalapi.com/credentials-info)
- [Portal de FiscalAPI](https://fiscalapi.com)
- [Sdk Python](https://github.com/FiscalAPI/fiscalapi-python)
- [Soporte técnico](https://fiscalapi.com/contact-us)
- [Certificados prueba](https://docs.fiscalapi.com/tax-files-info)

---

Desarrollado con ❤️ por [Fiscalapi](https://www.fiscalapi.com)
