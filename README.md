# UD13 Modelo Relacional - Ejercicios

## Ejercicio 1

<img width="245" alt="image" src="https://user-images.githubusercontent.com/99056015/164912921-26e8dcab-f01c-4e6f-9f03-50b2aa4f1a3c.png">

**Atleta**(Ndorsal(pk),Nombre,id_relevo)

## Ejercicio 2

<img width="332" alt="image" src="https://user-images.githubusercontent.com/99056015/164912937-ccde1028-4592-4366-8665-54f1be2f5bea.png">

**Elemento**(Nombre_elem(pk),peso_atomico,simbolo,natomico).
**Compuesto**(Nombre_Comp(pk),estado).
**Elemento_compuesto**(id(pk),proporcion,id_nombre_elemento(fk),id_nombre_compuesto(fk))
**Gaseoso**(%Compuesto%,Coef_expan,Temp_lic).
**Liquido**(%Compuesto%,Densidad,Temp_evap).
**Solido**(%Compuesto%,Color,olor,dureza).

## Ejercicio 3

<img width="230" alt="image" src="https://user-images.githubusercontent.com/99056015/164912953-574f7d40-4a47-4aae-8619-04786700b0b1.png">


**Sucursal**(Nsucursal(pk),ciudad,activo);
**Cuenta**(Ncuenta(pk),Saldo);
**Cliente**(Dni(pk),Nombre,Apellidos,Direccion,Ciudad);
**Sucursal_cliente_cuenta**(id(pk),id_sucursal(fk),id_cuenta(fk),id_cliente(fk))
**Transaccion**(NTransaccion(pk),Fecha,TipoOperacion,Cantidad,id_Cuenta(fk));

## Ejercicio 4

<img width="296" alt="image" src="https://user-images.githubusercontent.com/99056015/164912963-ade9a9fc-1d3b-4967-89a4-4c19a1905717.png">


**Parque_Bombero**(Cod_Parque(pk),Nombre, Direccion, Telefono, Categoria).
**Coche**(NumCoche(pk),Modelo,Marca,Num_Matricula,Fecha_compra,Fecha_ult_rev,id_parque_bombero(fk)).
**Equipo**(Cod_equi(pk),nombre).
**Peticion_Servicio**(CodPetServ(),Tipo_serv,GradoUgencia,Fecho,Hora,id_equipo(fk)).
**ParqueBombero_PeticionServicio**(id(pk),id_parque_bombero(fk),id_peticion_servicio(fk)).
**Bombero**(Cod_Bom(pk),Nombre,Apellidos,Fecha_Nac,Dni,Direccion,Telefono,id_parque_Bombero(fk),id_equipo(fk)).
**Periodo**(Fecha inicio(pk), Fecha fin(pk)).
**Turno**(Cod_Turno(pk),descripcion).
**Bombero_Turno_Periodo**(id(pk),id_periodo(fk),id_turno(fk)).

## Ejercicio 5

<img width="283" alt="image" src="https://user-images.githubusercontent.com/99056015/164912981-6dca878a-9773-461f-a79f-dbcb2d793ff6.png">


**Fondo**(Titulo(pk), Autor(pk), cantidad);
**Libro**(Signatura(pk),Dispnible,id_fondo(fk));
**Socios**(Nsocio(pk),nombre,Apellidos,Telefono,Fecha_cad);
**Prestamo**(Nprestamo(pk),fecha_prest,id_libro(fk),id_socio(fk));
**Prestamo_S**(%Prestamo%);
**Prestamo_E**(%Prestamo%,Fecha_Devol);
**Sanción**(NDias(pk), id_socios(fk));

## Ejercicio 6

<img width="257" alt="image" src="https://user-images.githubusercontent.com/99056015/164912988-69b96c85-36b5-4b39-bfbe-66989274cf74.png">

**Cliente**(cod_cliente(pk));
**Proveedor**(cod_proveedor(pk),unidades,fecha_encargo);
**Pedido**(cod_pedido(pk),fecha_pedido,id_cliente(fk));

**Producto**(cod_producto(pk), cantidad,id_producto(fk),id_proveedor(fk));

## Ejercicio 7

<img width="393" alt="image" src="https://user-images.githubusercontent.com/99056015/164912996-8315e36e-c72c-44dd-b5a4-cb13a9eef362.png">


**Arrendatario**(cif(pk),nombre_fiscal,nombre_firmante,cargo_firmante,direccion,codigo_postal,localidad,provincia,telefono_fijo,telefono_movil,fax,actividad);
**Nave**(codigonave(pk),poligono,calle,numero,localidad,codigo_postal,provincia,telefono,caracteristicas,foto,datos_escritura,alquilada,gastos_comunidad,id_arrendatario(fk));
**Recibo**(numero_recibo(pk),importe_total,importe_total,importe_iva,pagado,fecha,id_nave(fk),id_arrendatario(fk))

## Ejercicio 8

<img width="297" alt="image" src="https://user-images.githubusercontent.com/99056015/164913015-fa57a76c-165b-4fca-977d-64b5d413315a.png">

**Anotacion**(codigo_anotacion(pk),fecha,importe);
**Ingreso_Extra**(%Anotacion%,concepto);
**Tipo_gasto_fijo**(codigo_tipo_gesto(pk),nombre,descripcion);
**Gasto_fijo**(%Anotacion%,fecha_inicio,fecha_fin,consumo,id_tipo_gasto_fijo(fk));
**Gasto_Variable**(%Anotacion%,fecha_factura,concepto,numero_factura);
**Piso**(puesta(pk),dni,nombre,apellidos,direccion,codigo_postal,localidad,provincia,telefono);
**Ingreso_recibo**(%Anotacion%,mes,pagado,id_piso(fk),id_detalleRecibido(fk));
**DetalleRecibo**(numero_linea(pk),concepto,importe,id_ingreso_recibido(fk));
**Cargo**(codigo_cargo(pk),nombre,funciones);
**Piso_cargo**(id_piso_cargo(pk),id_piso(fk),id_cargo(fk),fecha)












