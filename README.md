# P01_ADBD - Modelo entidad/relación. Farmacia
## Aday Cuesta Correa y Manuel José Sebastían Noda
## Descripción de cada una de las entidades definidas
1. **Medicamentos**: En esta entidad se recoge todo lo relacionado con los medicamentos, desde su tipo y familia hasta las unidades en stock, etc.
2. **Laboratorios**: Esta otra entidad se encarga de almacenar los datos necesarios de los laboratorios con los que la farmacia trata. Posee datos identificativos de cada uno.
3. **Pedidos**: Esta entidad es la encarga de llevar el recuento de pedidos que se hacen de un medicamento y su fecha de compra
4. **Clientes**: Por último, tenemos la entidad de los clientes que realizan los pagos con créditos, aquí se almacena su número de cuenta bancaria y la fecha en la que realizan los pagos.
## Descripción y ejemplos ilustrativos del dominio de cada uno de los atributos de las entidades y de las relaciones.
### **Medicamentos**
En esta entidad tenemos los siguientes atributos:
1. **Nombre**: Es el nombre del medicamento, no es un atributo primario porque puede existir, por ejemplo, más de 1 ibuprofeno.
2. **Código**: Es el código del medicamento, en este caso si que es un atributo primario pues no pueden existir 2 medicamentos diferentes con el mismo código.
3. **Tipo**: Es el tipo del medicamento (jarabe, comprimido, pomada, ...), no es un atributo primario porque pueden existir varios medicamentos cuya aplicación sea en pomada.
4. **Familia**: Es la familia del medicamento, no es un atributo primario porque pueden existir medicamentos diferentes de la misma familia.
5. **Unidades en Stock**: Es el número de unidades del medicamento que aún quedan en el almacen, no es un atributo primario pues varios medicamentos distintos pueden tener el mismo número de existencias. 
6. **Unidades Vendidas**: Es el número de unidades que se han vendido de un medicamento, no es un atributo primario pues varios medicamentos pueden haber vendido el mismo número de unidades.
7. **Precio**: Es el precio del medicamento, no es un atributo primario pues varios medicamentos pueden costar lo mismo.
### **Laboratorios**
En esta entidad tenemos los siguientes atributos:
1. **Código del Laboratorio**: Es el código del laboratorio, es decir, lo que lo identifica. Es un atributo primario pues no queremos que hayan varios laboratorios con el mismo código.
2. **Nombre**: Es el nombre del laboratorio, si bien es una manera de identificar el laboratorio, no es atributo primario pues cabe la posibilidad de que se llamen igual, pero como possen distinto código se les puede diferenciar.
3. **Dirección Postal**: Es la dirección en la que se encuentra el laboratorio, es un ***atributo compuesto*** por los siguientes atributos:
 - **Nombre de la calle y número**: Es el nombre de la calle y su número.
 - **Localidad**: La localidad en la que se encuentra el laboratorio.
 - **Código Postal**: Código Postal del laboratorio.
 - **País**: País en el que se encuentra el laboratorio.
4. **Nombre Persona de Contacto**: Es el nombre de la persona con la que la farmacia contacta, no es un atributo primario pues varias personas pueden tener el mismo nombre.
5. **Fax**: Pueden ser los faxes del laboratio, notese que digo faxes y no fax pues es un atributo multievaluado, quizás un laboratorio puede tener un fax para cada departamento, etc.
6. **Teléfono**: Pueden ser los distintos teléfonos del laboratorio, es un atributo multievaluado por lo mismo que comentamos antes.
### **Pedidos**
En esta entidad tenemos los siguientes atributos, aunque ninguno es un atributo primario:
1. **Unidades Vendidas**: Es el número de unidades vendidas, idealmente está relacionado con el número de unidades vendidas de medicamentos.
2. **Fecha de Compra**: Es la fecha en la que se realizó la compra del medicamento.
### **Clientes**
En esta entidad encontramos los siguientes atributos:
1. **Fecha de Pago**: Es la fecha en la que se realiza el pago cada mes (ocurre a final de mes), no es un atributo primario pues habrá más de un cliente suscrito a este plan de la farmacia, lo que da lugar a que varias personas hagan el pago el mismo día.
2. **Cuentra Bancaria**: Es el número de cuenta del cliente y obviamente es un atributo primario que sirve para identificar a cada cliente por separado.
