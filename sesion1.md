## Sesión 1

# 1. Introduccion a Python para Seguridad

## Previo a la sesion tomar/leer el training:
- [requests](https://requests.readthedocs.io/en/latest/)
- [asyncio](https://docs.python.org/3/library/asyncio.html)
- [pwntools](https://docs.pwntools.com/en/stable/)
- [boto3](https://boto3.amazonaws.com/v1/documentation/api/latest/index.html)
- [pycryptodom](https://pycryptodome.readthedocs.io/en/latest/)
- [venv](https://docs.python.org/3/library/venv.html)
- [http](https://docs.python.org/3/library/http.server.html)

# requisitos
* Darse de alta en [meetup](https://www.meetup.com/es-es/hack-the-box-meetup-guatemala/events/315006753/?eventOrigin=home_next_event_you_are_attending) y [telegram](https://t.me/+eP0cFXw7DlJiMDNh) para llevar asistencia, preguntas y respuestas y para los premios. 
* Linux nativo, VM, o sobre WSL2.
* Python 3 instalado (ya viene en linux)
* Burpsuite community y/o Caido community
* Cuenta en [WebSecurity Academy](https://portswigger.net/web-security/dashboard)


# Durante la sesión
## Demo
- Uso de requests para replay de requests de Burp y testing de APIs
- Uso de asyncio para enumeracion concurrente de endpoints
- Uso de pwntools para interaccion con servicios vulnerables y parsing de respuestas
- Uso de boto3 para enumeracion basica de IAM y configuraciones AWS
- Uso de pycryptodome para validar o romper implementaciones criptograficas debiles
- Uso de logging para instrumentar tooling reproducible

## Por qué funciona:
- HTTP tooling es la base de toda explotacion web moderna
- Concurrencia permite escalar enumeracion y fuzzing
- Exploit development requiere automatizacion de interacciones con servicios
- Cloud y crypto son superficies comunes de exposicion en entornos reales

## Qué podria fallar en la arquitectura
- APIs sin rate limiting o proteccion contra automation
- Credenciales y permisos cloud mal configurados
- Implementaciones criptograficas "a mano"/custom o incorrectas
- Falta de observabilidad en tooling y ataques

## Tarea/Milla esxtra
- Crear script con requests para autenticar y consumir una API: simple request-response + pretty printing es sufieciente
- Crear script async para enumerar endpoints: Tipo ffuff super lite, se pueden usar diccionarios hardcoded, en un archivo externo o de SecLists.
- Crear script con pwntools para interactuar con un servicio vulnerable: Mi recomendaciòn son los retos de pwn.college para probar esto
- Crear script boto3 para listar recursos IAM basicos.

## Entregable
- script_X.py donde X indica que hace el script: Fuzzer, scanner, reqresponse, etc
- writeup.md: Explicando que hace el script, por què decidieron hacerlo?