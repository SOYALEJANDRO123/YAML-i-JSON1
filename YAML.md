# YAML: Lenguaje de Serialización de Datos

**YAML**, conocido como "YAML Ain't Markup Language," es un lenguaje de serialización de datos utilizado para diseñar archivos de configuración. 
Aunque algunos lo consideran otro lenguaje de marcado, su acrónimo refleja la idea de que se enfoca en datos en lugar de documentos.
# Usos de YAML

Uno de los usos comunes es la creación de archivos de configuración. Ansible® aprovecha la flexibilidad de YAML en sus playbooks, facilitando la automatización de procesos.

## YAML en Ansible

Los playbooks de Ansible, archivos YAML, organizan procesos de TI definiendo estados deseados. Utilizan módulos escritos en diversos lenguajes convertibles a JSON. La linterna `ansible-lint` ayuda a evitar errores.

## YAML para Kubernetes

Kubernetes usa archivos YAML para definir objetos y estados en un clúster, permitiendo a los desarrolladores comunicar la carga de trabajo deseada.

## Motivos para Elegir Red Hat

**Red Hat Ansible Automation Platform** utiliza YAML para compartir, evaluar y gestionar contenido de automatización. Ofrece herramientas como playbooks y sistemas de análisis, centralizando y controlando la infraestructura de TI.

**Red Hat OpenShift**, el Kubernetes empresarial, proporciona una plataforma sólida para desarrolladores, facilitando la creación, alojamiento e implementación de aplicaciones en la nube.
fuente: https://www.redhat.com/es/topics/automation/what-is-yaml.

## Sintaxis básica de YAML

Cada YAML comienza con `---` que denota el inicio de un archivo YAML.

**Espacios en blanco:** La sangría de espacio en blanco se utiliza para indicar el anidamiento y la estructura general.

**Matriz asociativa:** Una matriz asociativa está rodeada por corchetes (`{...}`). Las claves y los valores están separados por dos puntos (`:`) y cada par está separado por una coma (`,`).  
Ejemplo: `{name: John Smith, age: 20}`

**Cadenas:** La cadena se puede escribir con o sin comillas dobles (`"`) o comillas simples (`'`).  
Ejemplo: 

**Documentos múltiples:** Los documentos múltiples están separados por tres guiones (`---`) en una sola secuencia. Los guiones indican el inicio del documento. También se utilizan para separar las directivas del contenido del documento. El final del documento se indica con tres puntos (`...`).  
Ejemplo:   
```yaml
---
Documento 1
---

  ---
Documento 2
...
**Tipo:** Para especificar el tipo de valor se utilizan dobles signos de exclamación (!!).
Ejemplo: a: !!flotador 123
b: !!str 123
**Etiqueta:** para asignar una etiqueta a una nota, se usa un ampersand (&) y para hacer referencia a ese nodo, se usa un asterisco (*).
Ejemplo :nombre: Juan Smith
facturar a: &id01
calle: |
123 Callejón Tornado
suite 16
ciudad: East Centerville
estado: Kansas

**Directivas:** los documentos YAML pueden estar precedidos por directivas en una transmisión. Las directivas comienzan con un signo de porcentaje (%) seguido del nombre y luego los parámetros separados por espacios.

Ejemplo : %YAML 1.2
  ---
Contenido del documento
fuente:https://docs.fileformat.com/es/programming/yaml/
## Diferencia entre YAML y JSON
| Característica                  | JSON                                      | YAML                                         |
|---------------------------------|-------------------------------------------|----------------------------------------------|
| ¿Qué es?                        | Un formato de serialización de datos para intercambio de datos estructurados. Da prioridad al uso de las aplicaciones antes que al uso humano. | Un formato de serialización de datos para intercambio de datos estructurados. Da prioridad al uso humano antes que al de las aplicaciones. |
| Principales casos de uso        | Ampliamente extendido en plataformas, lenguajes, comunicaciones de software distribuido, aplicaciones web, archivos de configuración y API. | Archivos de configuración en muchas herramientas y servicios de automatización, DevOps e infraestructura como código (IaC). |
| Legibilidad                     | Fácil.                                    | Lo más fácil.                                |
| Tipos de datos                  | Número, booleano, nulo, cadena, matriz y objeto. | Admite todos los tipos de datos mediante colecciones de datos anidados que comprenden secuencias, escalares y asignaciones. |
| Admite comentarios              | No.                                       | Sí.                                          |
| Admite objetos de datos como valores | Sí.                                   | No.                                          |
| Control de versiones            | Sí, pero no es tan sencillo analizar y comprender de un solo vistazo las diferencias entre las versiones. | Sí, y es fácil analizar y comprender de un solo vistazo las diferencias entre las versiones. |
fuente: https://aws.amazon.com/es/compare/the-difference-between-yaml-and-json/
