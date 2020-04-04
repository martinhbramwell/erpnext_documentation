<! - add-breadcrumbs ->
# Ítem

**Un Ítem es un producto o servicio ofrecido o comprado por su empresa.**

El término Ítem también es aplicable a las materias primas o componentes de productos que aún no se han producido (antes de que puedan venderse a los clientes). ERPNext le permite administrar todo tipo de ítems como materias primas, subconjuntos, productos terminados, variantes de ítems y ítems de servicio.

ERPNext está optimizado para la gestión detallada de sus ventas y compras. Si está en servicios, puede crear un Ítem para cada servicio que ofrezca. Completar el Item Master es muy esencial para la implementación exitosa de ERPNext.

Para acceder a la lista de elementos, vaya a:
> Inicio> Stock> Ítems y precios> Item

## 1. Requisitos previos
Antes de crear y usar un elemento, se recomienda que cree primero lo siguiente:

* [Grupo de ítems](/docs/user/manual/en/stock/item-group)
* [Almacén](/docs/user/manual/en/stock/warehouse)
* Una unidad de medida si es necesario

## 2. Cómo crear un ítem
1. Vaya a la lista de elementos, haga clic en nuevo.
2. Ingrese un Código de ítem, el nombre se completará automáticamente igual que el Código de ítem al hacer clic dentro del campo Nombre de ítem.
1. Seleccione un grupo de ítems.
1. Ingrese las unidades de stock de apertura y la tasa de venta estándar.
3. Guardar.
  ![Ítem guardado](/docs/assets/img/stock/item-saved.png)

### 2.1 Propiedades del ítem

  * **Nombre del Ítem:** El nombre del ítem es el nombre real de su producto o servicio.
  
  * **Código del Ítem:** El código del ítem es una forma abreviada para denotar su ítem. Si tiene muy pocos ítems, es recomendable mantener el nombre del ítem y el código del ítem. Esto ayuda a los nuevos usuarios a reconocer y actualizar los detalles del ítem en todas las transacciones. En caso de que tenga muchos elementos con nombres largos y la lista se ejecute en cientos, es recomendable codificar. Para comprender los nombres de los códigos de ítems, consulte [Codificación de Ítems](/docs/user/manual/en/stock/articles/item-codification). También puede generar un Código de ítem basado en una [Series de Nombres](/docs/user/manual/en/setting-up/settings/naming-series) habilitando esta función en [Configuración de Almacén](/docs/user/manual/en/stock/stock-settings#1-item-naming-by).
  
  * **Grupo de Ítems:** Grupo de ítems se utiliza para clasificar un ítem bajo varios criterios como productos, materias primas, servicios, subconjuntos, consumibles o todos los grupos de ítems. Cree su lista predeterminada de Grupo de Ítems en *Configuración > Grupo de Ítems* y preseleccione la opción mientras completa los detalles de su *Nuevo Ítem* en [Grupo de Ítems](/docs/user/manual/en/stock/item-group). Los grupos de ítems pueden ser subconjuntos, materias primas, etc., o según el caso de uso de su empresa.
  
  * **Unidad de Medida Predeterminada**: Esta es la unidad de medida predeterminada que usará para su producto. Pueden ser Nos, Kgs, Metros, etc. Puede almacenar todas las unidades de medida que su producto requerirá en *Configuración > Almacén > Unidad de Medida (UdM) (UOM)*. Estos se pueden preseleccionar mientras se llena un nuevo elemento utilizando el signo % para obtener una ventana emergente de la lista UdM. Visite la página [UdM](/docs/user/manual/en/stock/uom) para obtener más detalles.

### 2.2 Opciones al crear un elemento
* **Desactivado**: Si desactiva un Ítem, no puede seleccionarse en ninguna transacción.

* **Permitir Ítem Alternativo**: A veces, cuando se fabrica un bien terminado, puede que no haya material específico disponible. Si marca esto, puede crear y seleccionar un elemento alternativo de la lista Alternativa de elementos. Para obtener más información, visite la página [Opción Alternativa](/docs/user/manual/en/manufacturing/item-alternative).

* **Mantener Existencias:** Si mantiene existencias de este ítem en su inventario, ERPNext realizará una entrada en el libro mayor para cada transacción de este ítem. Asegúrese de mantener esta opción sin marcar al crear un ítem que no esté en stock (por encargo / ingeniero) o un servicio.

* **Incluir Ítem en Fabricación**: Esto es para ítems de materia prima que se utilizarán para crear productos terminados. Si el ítem es un servicio adicional como 'lavado' que se usará en la lista de materiales, no lo marque.

* **Tasa de Valoración**: hay dos opciones para mantener la valoración de las existencias. FIFO (primero en entrar, primero en salir) y media móvil. Para comprender este tema en detalle, visite [Valoración de ítems, FIFO y promedio móvil](/docs/user/manual/en/stock/articles/item-valuation-fifo-and-moving-average).

* **Tarifa de Venta Estándar**: al * crear * un ítem, al ingresar un valor para este campo se creará automáticamente un [Precio del ítem](/docs/user/manual/en/stock/item-price) en el backend. Introducir un valor después de que se haya guardado el elemento no funcionará. En este caso, el precio del ítem se crea a partir de cualquier transacción con el ítem. La tasa a la que venderá el ítem. Esto se obtendrá en Pedidos de ventas y Facturas de ventas.

* **Es un Activo Fijo**: marque esta casilla de verificación si este elemento es un activo de la empresa. Consulte el [Módulo de activos](/docs/user/manual/en/asset) para obtener más información.

* **Creación Automática de Activos en la Compra**: si el ítem es un activo de la empresa, marque esta casilla de verificación si desea crear activos automáticamente mientras compra este ítem a través de [Ciclo de compra](/docs/user/manual/en/buying/purchase-order). Consulte la [Página de activos](/docs/user/manual/en/asset/asset) para obtener más información.

* **Porcentaje de Asignación**: esta opción estará disponible solo cuando cree y guarde el elemento. Este es el porcentaje por el cual se le permitirá facturar en exceso o entregar en exceso este Ítem. Si no se configura, seleccionará entre [Configuración de stock](/docs/user/manual/en/stock/stock-settings#3-limit-percent).

* **Carga de una Imagen**: para cargar una imagen para su icono que aparecerá en todas las transacciones, guarde el formulario parcialmente lleno. Solo después de guardar su archivo, aparecerá el botón 'Cambiar' en el icono de imagen. Haga clic en Cambiar, luego haga clic en Cargar y cargue la imagen.

Para la India:

* **HSN/SAC**: Sistema Armonizado de Nomenclatura (HSN) y Código de Contabilidad de Servicios (SAC) para GST. Estos números están definidos por el gobierno y los diferentes ítems se clasifican en diferentes códigos. Se pueden agregar nuevos códigos HSN si no están presentes en la lista.
* **Tiene calificación nula o está exento**: para un ítem que está bajo GST, pero no se le aplica ningún impuesto. Por ejemplo: cereales.
* **No es GST**: para un ítem que no está cubierto por GST. Por ejemplo: gasolina.

## 3. Características

### 3.1 Marca y descripción

* **Marca**: si tienes más de una marca, guárdalas en Venta> Marca y preselecciona mientras llenas un Nuevo Ítem.
* **Descripción**: Descripción del ítem. El texto del Código del ítem se obtendrá de forma predeterminada.
  ![Marca y descripción del ítem](/docs/assets/img/stock/item-brand-description.png)

### 3.2 Códigos de barras

Los códigos de barras se pueden registrar en Ítems para escanearlos rápidamente y agregarlos en las transacciones. En la tabla de códigos de barras, puede agregar el [código de barras para escanear] de un ítem (/ docs / user / manual / es / stock / articles / track-items-using-barcode). Hay dos tipos de códigos de barras en ERPNext:

* **EAN**: El número de ítem europeo es un número de 13 dígitos. EAN es utilizado internacionalmente y reconocido por más sistemas POS.
* **UPC**: el Código de producto universal es un número de 12 dígitos. UPC generalmente se usa solo en EE. UU. Y Canadá.

### 3.3 Inventario

* **Vida útil en días**: Esto es para un producto [Lote](/docs/user/manual/en/stock/batch). El número de días después de los cuales el lote de producto quedará inutilizable. Por ejemplo, medicamentos.
* **Fin de vida útil**: para un solo ítem / producto, la fecha después de la cual será completamente inutilizable. Es decir, el ítem será inutilizable en transacciones y fabricación. Por ejemplo, está utilizando cristales de plástico para fabricar ítems durante los próximos 5 años después de los cuales desea usar cuentas de plástico.
* **Garantía**: para realizar un seguimiento de un período de garantía, es necesario que el ítem esté serializado. Cuando se entrega este ítem, la fecha de entrega y el período de vencimiento se guardan en el maestro del número de serie. A través del número de serie maestro, puede realizar un seguimiento del estado de la garantía.

  Un período de garantía es un período de tiempo en el que un producto comprado puede ser devuelto o intercambiado.

  ![Garantía del ítem](/docs/assets/img/stock/item-inventory.png)

* **Peso UOM**: la unidad de medida del ítem. Pueden ser Nos, Kilo, etc. La UM de peso que utiliza internamente puede ser diferente de la UM de compra.
* **Peso por unidad**: El peso real por unidad del ítem. Por ejemplo: 1 kilo de galletas o 10 galletas por paquete.
* **Tipo de solicitud de material predeterminado**: cuando crea una nueva solicitud de material para este ítem, el campo establecido aquí se seleccionará de forma predeterminada en la nueva solicitud de material. Esto también se conoce como 'sangría'.
* **Método de Valoración**: Seleccione el Método de Valoración ya sea FIFO o Media Móvil. Para saber más sobre los métodos de valoración, [haga clic aquí](/docs/user/manual/en/stock/articles/item-valuation-fifo-and-moving-average).

### 3.4 Reordenamiento automático
Cuando el stock de un ítem cae por debajo de una determinada cantidad, puede establecer un reordenamiento automático en la sección 'Reordenamiento automático'. Esto debe habilitarse en [Configuración de stock](/docs/user/manual/en/stock/stock-settings#9-automatic-material-request). Esto generará una [Solicitud de material](/docs/user/manual/en/stock/material-request) para el Ítem. El usuario con roles de Administrador de compras y Administrador de existencias será ** notificado ** cuando se cree la Solicitud de material.

* **Check in (grupo)**: En qué almacenes de grupo verificar la cantidad del ítem.
* **Solicitud de**: Qué almacén para almacenar el pedido del ítem.
* **Nivel de reordenamiento**: cuando se alcanza esta cantidad, se activará el reordenamiento. El nivel de reordenamiento se puede determinar en función del tiempo de entrega y el consumo diario promedio. Por ejemplo, puede establecer el nivel de pedido de la placa base en 10. Cuando solo quedan 10 placas base en stock, el sistema creará automáticamente una solicitud de material en su cuenta ERPNext.
* **Cantidad de reordenamiento**: El número de unidades a reordenar para que la suma del costo de pedido y el costo de mantenimiento sea mínimo. La cantidad de reorden se basa en la 'Cantidad mínima de pedido' especificada por el proveedor y muchos otros factores.

  Por ejemplo, si el nivel de pedido es de 100 ítems, la cantidad de su pedido puede no ser necesariamente de 100 ítems. La cantidad de pedido puede ser mayor o igual que el nivel de pedido. Puede depender del tiempo de entrega, descuento, transporte y consumo diario promedio.

* **Tipo de solicitud de material**: El tipo [Solicitud de material](/docs/user/manual/en/stock/material-request) con el que se reordenará el stock. Esto depende de si compra el ítem, lo fabrica usted mismo o lo transfiere entre almacenes.

  <img alt = "Item Reorder" class = "screenshot" src = "{{docs_base_url}}/assets/img/stock/item-reorder.png">

> **Nota**: La solicitud de material se crea a las 12 de la medianoche, según el nivel de pedido establecido.

### 3.5 Unidades múltiples de medida
Puede agregar unidades de medida alternativas para un ítem. Si la UM predeterminada en la que vende es números (NoS) pero la recibe en Kilos, puede establecer una UM adicional con un factor de conversión apropiado. Por ejemplo, 500 Nos de tornillos = 1 kilogramo, seleccione Kilogramo / litro como UOM y establezca el factor de conversión en 500. Para obtener más información sobre cómo vender en diferentes unidades de medida, visite [esta página](/docs/user/manual/en/venta/ítems/Selling-in-different-UOM).

### 3.6 Números de serie

Con los números de serie, puede realizar un seguimiento de la garantía y las devoluciones. En caso de que el proveedor retire un ítem individual, el sistema de números ayuda a rastrear el ítem individual. El sistema de numeración también gestiona las fechas de vencimiento.

Tenga en cuenta que si vende sus ítems en miles, y si los ítems son muy pequeños, como bolígrafos o gomas de borrar, no necesita serializarlos.

En ERPNext, deberá mencionar el número de serie en algunas entradas contables. Si su producto no es un gran ítem duradero para el consumidor, si no tiene garantía y no tiene posibilidades de ser retirado del mercado, evite dar números de serie.

<img alt = "Serial No modal" class = "screenshot" src = "{{docs_base_url}}/assets/img/stock/serial_no_modal.gif">

### 3.7 Lotes

Se puede fabricar un conjunto de ítems en lotes. Esto es útil para mover el lote y asociar una fecha de vencimiento con un determinado lote.

* **Tiene número de lote**: las opciones para el número de lote, la fecha de vencimiento y el stock de muestra retenido se revelarán al marcar esta casilla. No puede activar esto si hay alguna transacción preexistente para este ítem. Si esto está deshabilitado, deberá ingresar los números de serie manualmente para cada transacción.

* **Serie de números de lote**: Prefijo que se aplicará a los números de lote. Si configura 5x1SCR, el primer lote se denominará como 5x1SCR00001 en la primera transacción / fabricación.

* **Crear nuevo lote automáticamente**: si el número de lote no se menciona en las transacciones, se crearán automáticamente de acuerdo con un formato como AAAA.00001. Si siempre desea crear manualmente un número de lote para este ítem, deje este campo en blanco. Esta configuración anulará el 'Prefijo de la serie de nombres' en la Configuración de archivo. Los números de lote se pueden configurar para que se generen automáticamente si fabrica los Ítems o se pueden ingresar manualmente si proviene de un fabricante externo.

* **Tiene fecha de vencimiento**: si marca esto, el número de lote se creará de acuerdo con la fecha de vencimiento. Las fechas de vencimiento se pueden establecer en el maestro 'Batch'.

* **Conservar muestra**: para conservar un número mínimo de stock de muestra del ítem. Para ello, debe establecer un Almacén de retención de muestra en Configuración de stock. Para saber más, [haga clic aquí](/docs/user/manual/en/stock/retener-sample-stock).

* **Tiene número de serie**: es similar a la serie de números de lote, se creará cuando realice transacciones / fabricación. Si configura la Serie de número de serie como AA, en la primera transacción se creará un número de serie como AA00001.

> Consejo: al ingresar un Código de ítem en una tabla de Ítems, si la tabla requiere detalles de inventario, dependiendo de si el ítem ingresado está en lotes o en serie, puede ingresar los números de serie o lote de inmediato en un cuadro de diálogo emergente.

<img alt = "Batch No modal" class = "screenshot" src = "{{docs_base_url}}/assets/img/stock/batch_no_modal.png">

> **Nota**: Una vez que marque un ítem como serializado o en lote o ninguno de los dos, no podrá cambiarlo después de haber realizado una Entrada de inventario.

Para obtener más información, visite la página [Reconciliación de stock](/docs/user/manual/en/stock/stock-reconciliation).

### 3.8 Variantes
Una variante de ítem es una versión diferente de un ítem. Para obtener más información sobre la gestión de variantes, consulte [Variantes de ítems](/docs/user/manual/en/stock/item-variantes).

### 3.9 Valores predeterminados del ítem

En esta sección, puede definir los valores predeterminados relacionados con las transacciones de toda la empresa para este ítem.

* **Almacén predeterminado**: Este es el Almacén que se selecciona automáticamente en sus transacciones con este ítem.
* **Lista de precios predeterminada**: Ya sea venta estándar o compra estándar. Del mismo modo, también puede configurar las cuentas predeterminadas de compra y venta
* **Proveedor**: si se establece un proveedor predeterminado, este se seleccionará para nuevas transacciones de compra.
* **Cuenta de gastos predeterminada**: Es la cuenta en la que se debitará el costo del Ítem.
* **Cuenta de ingresos predeterminada**: Es la cuenta en la que se acreditarán los ingresos por la venta del Ítem.
* **Centro de costos predeterminado**: Se utiliza para realizar un seguimiento de los gastos de este ítem.

  ![Valores predeterminados del ítem](/docs/assets/img/stock/item-defaults.png)

> Sugerencia: puede agregar más filas para varias empresas.

### 3.10 Detalles de compra, reabastecimiento

* **Unidad de medida de compra predeterminada**: la unidad de medida predeterminada que se utilizará en las transacciones de compra.
* **Cantidad mínima de pedido**: La cantidad mínima requerida para transacciones de compra como Órdenes de compra. Si se establece, el sistema no le permitirá continuar con la transacción de compra si la cantidad del ítem en la transacción de compra es menor que la cantidad establecida en este campo.
* **Stock de seguridad**: "Stock de seguridad" se utiliza en el informe "Nivel de pedido recomendado por ítem". Según el inventario de seguridad, el consumo diario promedio y el tiempo de entrega, el sistema sugiere el nivel de pedido de un ítem.

  Nivel de pedido = Stock de seguridad + (Consumo diario promedio * Tiempo de entrega)
* **Tasa de última compra**: La tasa a la que compró este ítem por última vez utilizando una [Factura de compra](/docs/user/manual/en/accounts/adquirir-factura) se mostrará aquí.
* **Es el ítem de compra**: Si no está marcado, no podrá usar este ítem en transacciones de compra.
* **Es el ítem proporcionado por el cliente**: Se verifica si el ítem es proporcionado por un cliente y se recibe a través de ** Entrada de stock> Recibo de material **. Si está marcada, el campo ** Cliente ** es obligatorio como el cliente predeterminado para ** Solicitud de material **. Para obtener más información, visite [esta página](/docs/user/manual/en/manufacturing/articles/customer-proporcionado-items).
* **Días de tiempo de entrega**: Los días de tiempo de entrega son el número de días entre el pedido y el Ítem para llegar al Almacén.

  <img class = "screenshot" alt = "Detalles de compra" src = "{{docs_base_url}}/assets/img/stock/item-purchase-details.png">

### 3.11 Detalles del proveedor

* **Entregado por el proveedor (Drop Ship)**: Si el proveedor entrega el ítem directamente al cliente, marque esta casilla de verificación. Más información [aquí](/docs/user/manual/en/selling/articles/drop-shipping).
* **Fabricante**: Seleccione el fabricante que fabricó este ítem.
* **Número de pieza del fabricante**: Ingrese el número de pieza del fabricante que el fabricante ha asignado a este ítem.
* **Códigos de proveedores**: Código de ítem de seguimiento definido por los proveedores para este ítem. En las transacciones de Compra, al seleccionar un Ítem, también se buscará un Número de Parte del Proveedor para referencia del Proveedor. Puede leer más al respecto [aquí](/docs/user/manual/en/shopping/articles/maintenance-Suppliers-part-no-in-item).

  ![Detalles del proveedor del ítem](/docs/assets/img/stock/item-supplier.png)

### 3.12 Detalles de comercio exterior
Si obtiene el ítem de otro país, puede configurar los detalles aquí.

* **País de origen**: el país del que obtiene el ítem.
* **Número de arancel de aduanas**: puede crear un número de arancel de aduanas con una descripción y usarlo como referencia aquí para compartirlo con las agencias de aduanas. Más tarde se puede usar para agregar notas de entrega.

### 3.13 Detalles de ventas

* **Unidad de medida de ventas predeterminada**: la unidad de medida predeterminada que se buscará para las transacciones de ventas.
* **Descuento máximo (%)**: puede definir el descuento máximo en% que se aplicará a un ítem. Por ejemplo: si establece el 20%, no puede vender este ítem con un descuento superior al 20%.
* **Es ítem de ventas**: si no está marcado, no podrá usar este ítem en transacciones de ventas.

  ![Detalles de ventas de ítems](/docs/assets/img/stock/item-sales.png)

### 3.14 Ingresos diferidos y gastos diferidos
Puede habilitar los ingresos o gastos diferidos del ítem. Una vez que marque la casilla de verificación, verá las opciones para configurar la Cuenta de gastos diferidos y la cantidad de meses a través de los cuales se difieren los ingresos / gastos.

Por ejemplo, considere una membresía anual al gimnasio, usted paga el dinero por adelantado de una vez, pero el servicio se brinda durante todo el año. Para el propietario del gimnasio, se trata de ingresos diferidos y para el cliente, es un gasto diferido.

  ![Ingresos diferidos](/docs/assets/img/stock/deferred-revenue.png)

Consulte las páginas en [Ingresos diferidos](/docs/user/manual/en/accounts/deferred-revenue) para obtener más detalles.

### 3.15 Detalles del cliente

El cliente puede identificar un ítem con un código de ítem diferente. esto es similar a [Código de proveedor](/docs/user/manual/en/stock/item#311-supplier-details).

* **Nombre del cliente**: Seleccione un cliente aquí.
* **Grupo de clientes**: se obtendrá en función del cliente que seleccionó en el campo anterior.
* **Código de referencia**: Un cliente puede identificar este ítem con un número diferente. Puede rastrear el código de ítem asignado por el cliente para este ítem. Cuando cree un pedido de cliente, se mostrará el código de referencia del cliente para este ítem.

### 3.16 Impuesto de ítem

Esta configuración es necesaria solo si un ítem en particular tiene una tasa de impuestos diferente a la tasa definida en la cuenta de impuestos estándar.

Debe crear una nueva 'Plantilla de impuestos de ítems' o elegir una existente. Por ejemplo, si tiene una cuenta de impuestos, “IVA 14%” y este ítem en particular está exento de impuestos, entonces selecciona “IVA 14%” en la primera columna y establece “0” como la tasa de impuestos en la segunda columna. . Visite la página [Plantilla de impuestos de ítems](/docs/user/manual/en/accounts/item-tax-template) para obtener más detalles.

 ![Plantilla de impuestos de ítems](/docs/assets/img/stock/item-tax-template.png)

También puede establecer una [Categoría de impuestos](/docs/user/manual/en/accounts/tax-category) para este Ítem.


### 3.17 Criterios de inspección

* **Inspección requerida antes de la compra**: Si una inspección es obligatoria antes de comprar el ítem, es decir, antes de generar el Recibo de compra, marque esta casilla de verificación.
* **Inspección requerida antes de la entrega**: Si se requiere una inspección en el momento de la entrega de su proveedor, es obligatorio para este ítem, marque esta casilla de verificación. Es decir, antes de generar un albarán de entrega.
* **Plantilla de inspección de calidad**: si se prepara una inspección de calidad para este ítem, esta plantilla de criterios se actualizará automáticamente en la tabla de inspección de calidad de la inspección de calidad. Ejemplos de criterios son: peso, longitud, acabado, etc.

La inspección de calidad se puede hacer con Vista rápida y no necesita ir a una página diferente para actualizar la inspección de detalles en ERPNext.

Para saber más sobre la inspección de calidad, [haga clic aquí](/docs/user/manual/en/stock/quality-inspection).

### 3.18 Fabricación

* **Lista de materiales predeterminada**: La [Lista de materiales] predeterminada (/ docs/user/manual/es/manufacturing/bill-of-materials) utilizada para fabricar este Ítem.
* **Suministro de materias primas para la compra**: si está subcontratando a un proveedor, puede optar por proporcionarles las materias primas para fabricar el ítem utilizando la lista de materiales predeterminada.

### 3.19 Sitio web

* **Mostrar en el sitio web**: elija si desea mostrar este elemento en su sitio web. Una vez que marque esto, se verán opciones adicionales para configurar el elemento en su sitio web. Para ver el elemento en el sitio web, haga clic en el enlace 'Ver en el sitio web' en la parte superior izquierda, justo encima de la imagen del elemento. Visite el [Módulo del sitio web](/docs/user/manual/en/website) para obtener más información.

  <img class = "screenshot" alt = "Detalles de fabricación" src = "{{docs_base_url}}/assets/img/stock/item-manufacturing-website.png">

* **Peso**: los ítems con mayor peso se mostrarán primero en el sitio web. El límite para el número que puede ingresar aquí es muy alto.

* **Presentación**: se puede mostrar una presentación en la parte superior de la página. Visite la página [Página de inicio](/docs/user/manual/en/website/homepage) en el módulo del sitio web para obtener más información.
* **Imagen**: puede adjuntar una imagen en lugar de una Presentación de diapositivas.
* **Almacén del sitio web**: Seleccione un almacén existente o cree un nuevo almacén para transacciones a través de su sitio web. Este Almacén será diferente de sus Almacenes fuera de línea. El stock para cualquier transacción en línea se deducirá de los Almacenes establecidos en el Almacén del sitio web.
* **Grupos de elementos del sitio web**: en esta tabla puede seleccionar los [Grupos de elementos] existentes (/ docs/user / manual / es / stock / item-group) para clasificar los elementos en su sitio web.
* **Establecer metaetiquetas**: las metaetiquetas ayudan con el SEO. Consulte [Página web](/docs/user/manual/en/website/web-page) para saber cómo agregarlos.

Visite [Fabricación](/docs/user/manual/en/manufacturing) y [Sitio web](/docs/user/manual/en/website) para comprender estos temas en detalle.

### 3.20 Especificaciones del sitio web
Esta sección es para configurar otros detalles sobre el ítem.

* **Copia del grupo de elementos:**: Los detalles de las 'Especificaciones del sitio web' se obtendrán tal como se establece en un Grupo de elementos específico elegido en la sección anterior (2.17).
* **Especificaciones del sitio web**: Etiqueta y su descripción para el ítem. Por ejemplo, 'Garantía: 1 año'.
* **Descripción del sitio web**: Esto aparecerá en la página del ítem.
* **Contenido del sitio web**: (*Introducido en v12*) Puede crear estilos adicionales, etc., use el marcado Bootstrap 4 para mostrar en la página del elemento.

### 3.21 Detalles de publicación de Hub

El hub es un mercado en línea gratuito donde los Proveedores y Clientes pueden realizar transacciones. Si ambas partes están en ERPNext, las transacciones se realizan sin problemas. Puede visitar el centro en: https://hubmarket.org.

* **Publicar en Hub**: elija si desea publicar su ítem en https://hubmarket.org/. Es un mercado libre. Si su proveedor / cliente también está en ERPNext, las transacciones serán perfectas. Por ejemplo, al crear una orden de compra a partir de su final, se creará una orden de venta al final del proveedor.
* **Hub Warehouse**: Este es un Warehouse separado para mantener el stock para sus transacciones de hub.
* **Sincronizado con Hub**: Sincronice el elemento y otros detalles con el hub cuando se realicen las transacciones.

## 4. Video

<div>
  <div class = 'embed-container'>
    <iframe
      width="840"
      height="473"
      src="https://www.youtube.com/embed/FcOsV-e8ymE"
      frameborder="0"
      allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen>      
    </iframe>
  </div>
</div>

### 5. Temas relacionados
1. [Precio del ítem](/docs/user/manual/en/stock/item-price)
1. [Codificación del ítem](/docs/user/manual/en/stock/articles/item-codification)
1. [Variantes del ítem](/docs/user/manual/en/stock/item-variants)
1. [Grupo de ítems](/docs/user/manual/en/stock/item-group)
1. [Atributo del ítem](/docs/user/manual/en/stock/item-attribute)
1. [Valoración de ítems FIFO y media móvil](/docs/user/manual/en/stock/articles/item-valuation-fifo-and-moving-average)
1. [Transacciones de valoración de ítems](/docs/user/manual/en/stock/articles/item-valuation-transactions)
1. [Mantener campo de inventario congelado en maestro de ítems](/docs/user/manual/en/stock/articles/maintenance-stock-field-frozen-in-item-master)
1. [Gestión de ítems de productos terminados rechazados](/docs/user/manual/en/stock/articles/managing-rejected-finished-goods-items)
1. [Devolver ítem rechazado](/docs/user/manual/en/stock/articles/return-rejected-item)
1. [Seguimiento de elementos utilizando código de barras](/docs/user/manual/en/stock/articles/track-items-using-barcode)
1. [Creación de depreciación para ítem](/docs/user/manual/en/stock/articles/creating-depreciation-for-item)
1. [Nombre del número de serie](/docs/user/manual/en/stock/articles/serial-no-naming)
1. [Ingreso de saldo de stock de apertura para ítem serializado y por lotes](/docs/user/manual/en/stock/articles/opening-stock-balance-entry-for-serialized-and-batch-item)
1. [Número de serie](/docs/user/manual/en/stock/serial-no)
1. [Nombre del número de serie](/docs/user/manual/en/stock/articles/serial-no-naming)
