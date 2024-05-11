LOTOTYPE Admin frontend

Descripcion del Proyecto: 
LOTOTYPE es una plataforma que permite que representantes (personas dueñas de los sorteos) hagan sorteos de loteria mexicana (10 cartones maximo), bingo hasta 100 cartones, de forma automatica


Tecnologias a utilizar: 
La tecnologia frontend sera angular, conforme al template html

Requerimientos funcionales de interfaz de manager de sorteos (admin)
1	Lototype agregara un nuevo usuario (representante) con los siguientes datos, id, nombre completo, telefono, numero de identificacion (DUI), y contraseña para dar de alta a un nuevo representante. Esta parte lo ejecutara LOTOTYPE directamente en base de datos. (saveManager)

2	“Contraseña” interfaz para cambiar la contrasena en la tabla manager. (managerChangePass)

3	El representante tendra una interfaz para subir su logo (según tamaño definido) nombre de la casa, slogan primario, slogan secundario “Manager”. La vista de esta parte aun no esta definida, pero debe de ser una url con login aparte y que su apariencia sea con bootstrap, con menu (updateManager) (getManager)

4	El manager tendra una interfaz de configuracion de pagos, y podra realizar pagos a LOTOTYPE para evitar deshabilitacion Pagos.Proveedor, . La vista de esta funcion no esta definida pero se solicita que tenga la misma apariencia de la plantilla. (el pago del servicio sera calculado mas adelante) 
(saveServicePayment deshabilitar se hace desde pago paypal) (getServicePayments)

5	El manager tendra una pantalla “Pagos”manual, en la que podra visualizar las solicitdes de pago y retiro por medio de los clientes, transacciones que aprobara luego de revisar su cuenta bancaria, esta tabla se llenara desde frontend id, nombre competidor, tipo de pago, estado, fecha de pago (savePaymentPetition deshabilitar se hace desde fe) (getPaymentsPetition) (paymentPetitionApprove) (paymentPetitionDeny) falta busqueda por nombre competidor

6	El manager tendra un interfaz para programar sorteos “Sorteos”, los cuales tendran los siguientes datos, nombre de conjunto de sorteos, numero de sorteos, premio en dolares, precio de carton en dolares, numero maximo de cartones a incluir en cada sorteo, numero total de sorteos a realizar de forma procedural, el cual se podra activar o desactivar. (lottery, id, id_manager, lotteryname varchar 150, lotterycount int 100, prize float 7.2, cardprice float 7.2, maxcards int 2, active int 1(0,1), datelottery datetime. (saveLottery) (getLotteries) falta busqueda por activas
7	El manager tendra un interfaz consultar sus transacciones “compras”, los cuales tendran los siguientes datos, nombre de loteria, nombre de competidor, monto de (lotteryBuy) (getAllBuyLotteries)

8	El manager tendra en un dashboard en el cual tendra los siguientes datos: total de ganacias mes, total de pagos mes, diferencia mes, total de ganancias, total de pagos, un grafico de las ganancias totales en los ultimos 5 meses, total de ganancias las cuales se iran sumando en la tabla lottodash (Abono, Retiro).

Los montos del grafico de ganancias netas de los ultimos 5 meses seran calculadas teniendo en cuenta las tablas moneylotto filtrada por id_manager(endpoint aun no definido)

9	El representante tendra un interfaz para programar sorteos “Sorteos”.Bingo, los cuales tendran los siguientes datos, nombre de conjunto de sorteos, numero de sorteos, premio en dolares, precio de carton en dolares, premios (3, do opcionales)numero minimo de cartones a incluir en cada sorteo, numero total de sorteos a realizar de forma procedural, numero de cartones a vender (20,30,60,90) a generar, el cual se podra activar o desactivar (saveLottery) (getLotteries) (getActualLotteries) (saveBingo) (getBingos) (getActualBingos)



-	En este repositorio esta el template html a utlizar y la colección de postman, se habilitara las apis backend para quien haga el trabajo
