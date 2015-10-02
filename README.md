# Arquitectura FrontEnd en Schibsted Spain #

## ¿Qué es Schisted?

Empresa dedicada a clasificados. Con varios verticales.

[@joan poner screenshot verticales]

## Motivación

Acabar con el monolito en el front-end

## Donde vamos

Componentes + UI reutilizable

## Requisitos

* Diseño orientado a componentes (Objetos inteligentes de PS)
* F.E. enfocados a clean code (no más spaghetti code)
* B.E. orientado a API´s (microservicios)

* Todo tiene que ser Open Source
* Cualquier tecnología de UI es caduca.

## Independencia del monolito:

[@joan Aqui ponemos la gráfica del proxy, monolito, backend]

## Maxima reutilizacion de los componentes

[@joan aquí la mención a la Arch Onion => Arch Minion!!]

[@joan aquí va el diagrama de capas de cebolla]

## Como montamos esto

* Código homogéneo
* Service discovery
* Reutilización de código
* Independencia de la solución
* Problemas


### Código homogénio:

* Generador:

	Tdd, autoreload y todo lo necesario para desarrollar tu componente
	Publicación automática de la demo a una página de github pages
	
* Reglas de precommit:

  * Estan versionadas (https://github.com/scm-spain/frontend-pre-commit-rules)
  * Son instalables `npm i @schibstedspain/frontend-pre-commit-rules`

### Service Discovery (más o menos)

* npm enterprise (namespace: @schibstedspain)
* SUI Component Organización https://github.com/SUI-Components

### Reutilización de código

* Contenedor contenido 

	[@joan aquí iría el diagrama de cajitas]
	
* sui-component (Open source)
* re, ij, mt *-Components (privados/reglas de negocio)
* Themebles (SUIT)
  * Theme basic (npm i @schibstedspain/theme-basic)
  * Theme re, ij, (npm i @schibstedspain/re-theme-fotocasa)
  
### Independencia de la solucion

* Framework volátiles
	[@joan aquí ponemos la viñeta de los frameworks]
	
* Solución:
  * `npm install real-estate`
  
	[@joan aquí tendría que ir algo rollo Dominio -> Dominion!!!]
  
  * Cuando cambiemos la tecnología de UI reutilizamos todas las reglas de negocio:
    * Llamadas a otros sistemas
    * Validaciones
    * Calculos
	
  
### Problemas
* I18N (No depende de la tecnología de UI) (Rosseta)
* Tracking (Suntory)
* HTML con reglas de negocio, Malo para el open source

### BTW

Usamos ReactJS para pintar el DOM




