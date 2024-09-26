# P01_ADBD - Modelo entidad/relación. Farmacia
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
5. **Unidades en Stock**:
6. **Unidades Vendidas**:
7. **Precio**:
