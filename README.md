# Laboratorio de Diseño Electrónico CAD — KiCad 10

**Curso:** Diseño Electrónico CAD  
**Autores:** Alejandro Beltrán Cardona, Daniel Zuluaga González y Jhon Alexander Salazar Rendón.  
**Fecha:** octubre de 2026.

## Contenido

- `Ejercicio_1_Linterna/`: linterna LED alimentada con pila CR2032, pulsador y resistencia limitadora.
- `Ejercicio_2_ESP32_S3_Mini/`: tarjeta compacta ESP32-S3 con regulación AMS1117-3.3, botón BOOT y USB.
- `Ejercicio_3_ESP32_S3_USB_C_PCBA/`: placa ESP32-S3 avanzada con USB-C, CP2102N, protección ESD, autoprogramación y conectores GPIO.

Todos los proyectos son de **dos capas de cobre**. Cada carpeta incluye los archivos `.kicad_pro`, `.kicad_sch` y `.kicad_pcb` originales. El ejercicio 2 incluye además la biblioteca de símbolo y huella personalizada, configurada con rutas relativas al proyecto.

## Cómo abrir

1. Instalar KiCad 10.x.
2. Entrar en la carpeta del ejercicio deseado.
3. Abrir el archivo `.kicad_pro` correspondiente.
4. Para revisar los circuitos y las placas, usar el editor esquemático y el editor PCB.
5. Antes de fabricar, ejecutar ERC/DRC con las reglas compatibles con el fabricante y comprobar las exclusiones o pruebas ignoradas.

## Fabricación y ensamblaje

Los archivos Gerber/Excellon se exportan desde el editor PCB de cada ejercicio. La tarjeta 3 también requiere BOM y CPL/posiciones para la cotización PCBA. **Este repositorio incluye los proyectos fuente; no implica que se hayan fabricado físicamente, comprado o ensamblado las tarjetas.**

El importe de fabricación depende de las especificaciones y de la cotización actual de JLCPCB. Verifique límites de manufactura, el manejo de la antena RF y la coincidencia real entre BOM, componentes disponibles y huellas.

## Nota

No se incluyen las carpetas `.history/.git` (historial local de la herramienta), archivos de sesión `.kicad_prl`, copias de seguridad o binarios temporales. El circuito y la PCB no se han modificado en el proceso de organización del repositorio.

## Cotizaciones JLCPCB: 27 de octubre de 2026

Captura: `Cotizaciones_JLCPCB/cotizacion_carrito_jlcpcb_27_10_2026.png`.

| Concepto | 5 unidades | Precio observado (USD) |
|---|---:|---:|
| PCB linterna LED | 5 | 20,66 |
| PCB ESP32-S3 Mini | 5 | 4,00 |
| PCB ESP32-S3 USB-C | 5 | 4,00 |
| PCBA estándar SMT superior ESP32-S3 USB-C | 5 | 123,36 |
| **Suma de partidas visibles** | | **152,02** |

El precio de PCBA indica *Assemble top side* y no demuestra montaje completo de pines/pulsadores THT o ensamblaje inferior. Valores sin verificación de envío e impuestos. La cotización no es un pedido pagado.

El informe IEEE actualizado se encuentra en `Informe_IEEE/`.