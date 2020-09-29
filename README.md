# ReciklarDataBase
Alumno: Elías González C.

Esta es una actividad para la ayudantía del curso de Diseño de Software, impartida por el Sr. Paolo Caviedes.
Los comandos de los queries se encuentran al final del archivo .txt y a continuación:

-- QUERIES

-- 1.Obtener todos los clientes de Reciklar
SELECT * FROM CLIENTE;

-- 2.Obtener todos los retiros que han realizado para un cliente específico
SELECT FROM RELACION RETIRO WHERE CLIENTE_RUT = 'rut de client específico';

-- 3.Obtener todas las rutas realizadas entre 2 fechas
SELECT FECHA_idFECHA FROM RELACION RUTA WHERE FECHA_idFECHA BETWEEN 'AAAA.MM.DD.HH.mm' AND 'AAAA.MM.DD.HH.mm';

-- 4.Obtener el cliente con más retiros
SELECT CLIENTE_RUT FROM RELACION RETIRO GROUPED BY CLIENTE_RUT ORDER BY COUNT(*) DESC LIMIT 1;

--5.Obtener el retiro con más Kilogramos de desechos
SELECT MAX(PESO_idPESO) FROM RELACION RETIRO;

--6.Obtener una lista de clientes, retiros y residuos retirados
SELECT CLIENTE_RUT, FECHA_idFECHA, RESIDUO_Tipo Residuo FROM RELACION RETIRO;
