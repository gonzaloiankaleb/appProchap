# Prochap - Generación y Envío de PDFs de Chapas

Esta aplicación permite gestionar imágenes y archivos PDF relacionados con chapas y facilita el envío de estos archivos por correo electrónico a un cliente.

## Requisitos

- Python 3.x
- Las siguientes librerías deben estar instaladas:
  - `customtkinter`
  - `fpdf`
  - `PyPDF2`
  - `tkinter` (incluido en la instalación estándar de Python)
  - `webbrowser` (incluido en la instalación estándar de Python)

Para instalar las dependencias faltantes, ejecute el siguiente comando:

```bash
pip install customtkinter fpdf PyPDF2
```

## Funcionalidades

1. **Carga de archivos**: Permite seleccionar una imagen y un PDF.
2. **Generación de PDF**: Combina la imagen seleccionada y el PDF en un solo archivo PDF.
3. **Envío por correo**: Abre el cliente de correo predeterminado con el archivo PDF listo para ser enviado al cliente.

## Estructura del código

### Funciones principales

- **`validar_correo(correo)`**: Verifica si un correo tiene un formato válido.
- **`seleccionar_imagen()`**: Abre un cuadro de diálogo para seleccionar una imagen.
- **`seleccionar_pdf()`**: Abre un cuadro de diálogo para seleccionar un archivo PDF.
- **`generar_pdf_chapa(ruta_imagen, ruta_pdf, ruta_guardado)`**: Genera un PDF que combina una imagen y un PDF, guardándolo en la ruta especificada.
- **`abrir_cliente_correo(destinatario, ruta_pdf)`**: Abre el cliente de correo predeterminado con el archivo PDF adjunto.

### Clase `App`

- **Interfaz gráfica**: Utiliza `CustomTkinter` para mostrar una ventana que permite la selección de una imagen y un PDF, la generación del PDF final, y el envío por correo.

### Ejecución

El código se ejecuta a través de la siguiente instrucción:

```python
if __name__ == "__main__":
    app = App()
    app.mainloop()
```

Esto crea una instancia de la aplicación y ejecuta el ciclo principal para mostrar la interfaz gráfica.

## Uso de la aplicación

1. Ingrese el correo del cliente en el campo correspondiente.
2. Seleccione una imagen y un archivo PDF usando los botones correspondientes.
3. Haga clic en el botón **Generar PDF** para combinar los archivos seleccionados en un solo PDF.
4. Haga clic en **Abrir correo con PDF** para abrir su cliente de correo predeterminado con el PDF adjunto.

## Contribuciones

Creado por Gonzalo Rolon.

## Licencia

Este proyecto está bajo la licencia MIT.
