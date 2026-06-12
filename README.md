# Convio

![C++](https://img.shields.io/badge/C%2B%2B-17-blue)
![GPLv3](https://img.shields.io/badge/license-GPLv3-green)
![Linux](https://img.shields.io/badge/platform-Linux-orange)
![macOS](https://img.shields.io/badge/platform-macOS-lightgrey)
Convio es una herramienta de línea de comandos (CLI) de código abierto desarrollada en C++ para la conversión de archivos entre formatos compatibles. Utiliza un sistema de plugins dinámicos para permitir la adición de nuevos formatos de archivo sin necesidad de modificar el código base. Convio determina automáticamente una ruta de conversión entre formatos compatibles utilizando los plugins instalados. Convio es fácil de usar y altamente personalizable, lo que lo convierte en una solución ideal para desarrolladores, diseñadores y cualquier persona que necesite convertir archivos de manera eficiente.

## Características
- Soporte para una amplia variedad de formatos de archivo.
- Sistema de plugins dinámicos para la adición de nuevos formatos.
- Interfaz de línea de comandos fácil de usar.
- Personalización a través de opciones de configuración.
- Resolución automática de rutas de conversión.

## Compatibilidad
Convio actualmente es solo compatible con sistemas operativos basados en Unix, como Linux y macOS. No existen planes inmediatos para agregar soporte para Windows, pero las contribuciones relacionadas con esta funcionalidad serán bienvenidas.

## Construir desde el código fuente
1. Clonar el repositorio:
```bash
git clone https://github.com/CeccPro/convio.git
```

2. Navegar al directorio del proyecto:
```bash
cd convio
    ```

3. Compilar el proyecto:
```bash
make
```

4. Instalar la herramienta (opcional):
```bash
sudo make install
```

## Resolución automática de conversiones

Convio construye un grafo de formatos a partir de los plugins instalados y busca automáticamente una ruta válida entre el formato de origen y el de destino.

Ejemplo:

```text
PDF
↓
HTML
↓
DOCX
```

Si existe una ruta de conversión compatible, Convio la ejecutará automáticamente. Si no se encuentra una ruta, se mostrará un mensaje de error indicando que la conversión no es posible con los plugins disponibles.

## Uso
Para convertir un archivo, ejecuta `convio` indicando el archivo de entrada y la flag -o seguida del archivo de salida. Por ejemplo:
```bash
convio input.jpg -o output.png
```

Para obtener una lista completa de los formatos soportados y las opciones de configuración, puedes ejecutar:
```bash
convio --help
```

Para obtener una lista de los plugins disponibles, puedes ejecutar:
```bash
convio --list-plugins
```

Para listar todos los formatos en los que puedes convertir un archivo, puedes ejecutar:
```bash
convio input_file --list-formats
```
O en general para listar todos los formatos soportados:
```bash
convio --list-formats
```

## Estado del proyecto

Convio se encuentra actualmente en desarrollo activo.
La API de plugins y algunos formatos soportados pueden cambiar entre versiones. Se recomienda a los usuarios y desarrolladores que revisen regularmente el repositorio para mantenerse actualizados con los cambios y mejoras.

## Contribuir
Si deseas contribuir al proyecto, puedes seguir estos pasos:
1. Fork el repositorio.
2. Crea una nueva rama para tu característica o corrección de errores:
```bash
git checkout -b feature/nueva-caracteristica
```
3. Realiza tus cambios y haz commit de ellos:
```bash
git commit -m "Agrega nueva característica"
```
4. Empuja tus cambios a tu fork:
```bash
    git push origin feature/nueva-caracteristica
```
5. Abre un Pull Request en el repositorio original.

## Licencia
Convio está licenciado bajo la Licencia GNU General Public License v3.0 (GPLv3). Consulta el archivo LICENSE para más detalles.