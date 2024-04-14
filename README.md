# Semana 1

## Actividad

>Entregar un documento en formato markdown en el repositorio, en 
>la carpeta /docs, con todas las clases base detectadas como necesarias para 
>resolver el problema, con sus atributos, métodos y responsabilidades. 
>Entregar un modelo DER con todas sus entidades completas.

## Clases destacadas

### 1. Casilla

#### Atributos
    Número de Casilla
    Tipo de Casilla
    Propiedad (clase)
    Estado de la casilla (comprada, disponible, etc)
#### Métodos
    Método Salida
    Método Impuesto
    Método Premio Ganadero
    Método Destino
    Método Comisaría
    Método Descanso
    Método Free Parking
    Método Marche Preso
    Método Suerte
    Método Zonas
    Método Compañías
    Método Ferrocarriles
#### Responsabilidades
    Disparar el método de acción adecuado, en relación al tipo de casilla

---
### 2. Tablero

#### Atributos
    Lista de Casillas
    Lista de Tarjetas de Suerte o Destino (orden)
#### Métodos
    Mostrar Tablero
    Asignar turno	
#### Responsabilidades
    Iniciar y finalizar el juego
    Guardar y Recuperar las partidas.
    Asignar turnos a jugadores y avanzar casilleros
#### Responsabilidades
>

---
### 3. Dados

#### Atributos
    PrimerDado
    SegundoDado
#### Metodos
    Lanzar dados aleatoriamente 
#### Responsabilidades
    Lanzar dos números al azar cada vez que se lo pedimos

---
###	4. Ajustes

#### Atributos
>
###	Métodos
    Abandonar Partida
    Finalizar Partida
    Guardar Partida
### Responsabilidades
    Finalizar el juego
    Guardar la partida.
    Informar acerca del estado del juego en cualquier momento

---
### 5. Menu De Inicio

#### Atributos
    Lista de Jugadores
    Lista de Tarjetas de Suerte o Destino (orden)
    Estado del Juego (no activo, activo, finalizado)
    Permite Ganar por total (booleano)
    Valor Total Máximo
#### Métodos
    Configurar Partida
    Iniciar Partida
    Recuperar Partida
    Información del Juego
#### Responsabilidades
    Iniciar el juego
    Recuperar las partidas.
    Asignar turnos a jugadores casilleros

---
### 6.	Jugador

#### Atributos
    ID jugador
    Nombre Jugador
    Tipo de Jugador (virtual o real)
    Perfil Jugador (conservador, moderado, agresivo)
    Dinero
    Valor Hipotecado
    Posición en el tablero
    Prisionero (booleano sí o no)
    Lista de Provincias
    Lista de Compañías
    Lista de Ferrocarriles
    Turnos de Espera (cantidad de turnos de espera)
    Doble en dados (cantidad de veces que tiene doble)
    Deseo de Quedarse (booleano sí, no)
    Estado del jugador (en juego, abandonó, quebrado)
#### Métodos
    Tirar los dados
    Pagar dinero
    Cobrar dinero
    Comprar Propiedad
    Comprar chacra
    Comprar estancia
    Vender Propiedad
    Pedir cambio (¿?)
    Hipotecar Propiedad
    Abandonar el juego
#### Responsabilidades
    Ejecutar las acciones derivadas del juego de su turno en particular, como tirar los dados y decidir que hacer en virtud del resultado obtenido.

---
### 7.	Propiedad

#### Atributos
    ID propiedad (29 tarjetas)
    Tipo de Propiedad (campo, ferrocarril, compañía)
    Detalle
    Valor de la Propiedad
    Dueño (jugador o banco)
    Hipotecada (booleano si no)
    Valor Hipoteca
#### Métodos:
> 
#### Responsabilidades: 
>

---
### 8.	Campo (zona – HEREDADA DE PROPIEDAD)

#### Atributos
    Zona
    Provincia
    Chacras (cantidad)
    Estancias (booleano – tiene o no tiene)
    Valor de Chacra
    Valor de Estancia
    Valor Alquiler Campo
    Valor Alquiler Campo + 1 chacras
    Valor Alquiler Campo + 2 chacras
    Valor Alquiler Campo + 3 chacras
    Valor Alquiler Campo + 4 chacras
    Valor Alquiler Campo + 1 Estancia
#### Métodos
    Calcular Alquiler
#### Responsabilidades: 
    Debe poder devolver el valor del alquiler calculado en función de la situación.

---
### 9.	Compañía (heredada de Propiedad)

#### Atributos
    Valor teniendo 1
    Valor Teniendo 2
    Valor Teniendo 3
###	Métodos
    Calcular Alquiler
###	Responsabilidad
    Debe poder devolver el valor del alquiler calculado en función de la situación.

---
### 10. Ferrocarril (heredada de Propiedad)

#### Atributos
    Valor teniendo 1
    Valor teniendo 2
    Valor teniendo 3
####	Métodos
    Calcular Alquiler
###	Responsabilidad
    Debe poder devolver el valor del alquiler calculado en función de la situación.

---
### 11.	Tarjetas Suerte Destino

#### Atributos
    ID tarjeta
    Detalle
    Lista de Acciones (clase Acción Tarjeta)
####	Métodos
    Ejecutar Acción Tarjeta
#### Responsabilidades: 
>
---
### 12.	Acción Tarjeta Suerte Destino

####	Atributos
    ID Acción
    ID Tarjeta
    Tipo Acción
    Valor
    Cantidad
    Destinatario (jugador o banco)
#### Métodos:
> 
#### Responsabilidades: 
>

---
### 13.	Provincia

#### Atributos
    Id Provincia
    Denominación
    Lista de Campos (clase)
    Dueño (jugador)
#### Métodos
    Asignar Dueño
#### Responsabilidades:
    Contener la lista de campos de cada una y asignar el propietario cuando se cumpla la condición.

---
### 14.	Banco

#### Atributos
    Lista de Propiedades
    Dinero
    Chacras (cantidad)
    Estancias (cantidad)
####	Métodos
    Cobrar
    Pagar
    Hipotecar
    Entregar Propiedad
    Recibir Propiedad
    Entregar Cambio (billetes)
#### Responsabilidades: 
>
---
### 15.	Dinero

#### Atributos
    Lista de Billetes (Clase Billete)
#### Métodos
    Calcular Valor
#### Responsabilidades: 
    Determinar en cualquier momento el valor del dinero que tiene un jugador o el banco.

---
### 16.	Billete

#### Atributos
    ID billete
    Descripción
    Valor nominal
    Cantidad Total de esa denominación
#### Métodos:
> 
#### Responsabilidades: 
>