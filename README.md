# Fumigadora Fumicity
Proyecto realizado para la materia de Base de Datos,donde se hace la base de datos relacional para una empresa fumigadora con ayuda de OracleSQL, haciendo uso de PL/SQL

Autores: 
- JIMENEZ GARCIA RODRIGO GAUDENCIO
- ROMERO PEDRAZA FRANCESCA MELANIA
- SANTIAGO PEREZ DANIELA
- CUELLAR URIBE FERNANDO.

## Instalación de dependencias
No se requiere la instalacion previa de ningun libreria adicional, basta con tener un sistema linux con oracle 19C configurado.

En esta parte hemos implementado un script que nos automatiza la creacion de la base de datos, s-00-main.sql, por lo que se presentan las instrucciones para descargar el proyecto y ejecutar el script.

```bash
git clone https://github.com/RGJG28/BD_Fumigadora.git 
cd BD_Fumigadora
sqlplus usuario/contraseña@nombre_base_datos @s-00-main.sql
```
## Caso de estudio
La empresa fumigadora Fumicity requiere un sistema para gestionar información sobre sus servicios, empleados, sucursales y clientes. Las especificaciones son las siguientes:

- Sucursales: cada sucursal tiene un número único, número de teléfono y dirección. Cada sucursal tiene departamentos, incluyendo Ventas, Aplicación de Servicios y Mecánica, con un número de departamento único y correo electrónico.

- Empleados: hay cuatro tipos de empleados: Gerente, Vendedor, Técnico y Mecánico. Cada empleado tiene un número de empleado, RFC, nombre completo, correo, teléfono, fecha de nacimiento y salario mensual. El Gerente supervisa otros empleados. 
  El Vendedor puede tener turnos matutinos o vespertinos, trabajando a tiempo completo (9 horas) o medio tiempo (4.5 horas), y puede supervisar otros vendedores. El Técnico puede tener alergias, años de experiencia y usa un auto para trabajar. 
  El Mecánico tiene un año de ingreso y puede haber tomado capacitación. Además, el Mecánico repara los autos en caso de falla.

- Clientes: hay dos tipos, empresas y personas. Cada cliente tiene un número único, forma de pago (efectivo o tarjeta de crédito/débito) y ubicación. Se conoce el nombre de la empresa y el nombre completo y correo de las personas.

- Servicios: cada servicio tiene un identificador único, precio, tipo de plaga y tipo de lugar donde se realizará (restaurantes, oficinas, casas, camiones, bodegas y cajas secas).

- Productos y herramientas: los técnicos utilizan productos para fumigar, que se clasifican en Gel, Líquido y Aire. Se conocen el número y tipo de producto. Las herramientas, como Mangueras, Pistolas, Aplicadores de Gel y Aspersores, también se 
  identifican por número y tipo.

## Solución propuesta
![Modelo entidad-relación](https://github.com/RGJG28/BD_Fumigadora/blob/main/src/BD_proyecto_fumigadora_MER.png)
![Modelo relacional](https://github.com/RGJG28/BD_Fumigadora/blob/main/src/Proyecto_fumigadora_ET.jpg)

