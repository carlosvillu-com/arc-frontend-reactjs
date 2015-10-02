# Arquitectura FrontEnd en Schibsted Spain #

## ¿Qué es Schibsted?

Empresa dedicada a clasificados. Con varios verticales.

## Motivación

Acabar con el monolito en el frontend

## A dónde vamos

Componentes + UI reutilizable

## Requisitos

* Diseño orientado a componentes (Objetos inteligentes de PS)
* F.E. enfocados a clean code (no más spaghetti code)
* B.E. orientado a APIs (microservicios)

* Todo tiene que ser open source
* Cualquier tecnología de UI caduca pronto.

## Independencia del monolito:

[gráfica del proxy, monolito, backend]

## Máxima reutilización de los componentes

[diagrama de capas de cebolla]

## Cómo montamos esto

* Código homogéneo
* Service discovery
* Reutilización de código
* Independencia de la solución

### Código homogéneo:

* Generador:

	TDD, autoreload y todo lo necesario para desarrollar tu componente
	Publicación automática de la demo a una página de github pages
	
* Reglas de precommit:

  * Están versionadas (https://github.com/scm-spain/frontend-pre-commit-rules)
  * Son instalables `npm i @schibstedspain/frontend-pre-commit-rules`

### Service discovery 

* npm enterprise (namespace: @schibstedspain)
* SUI Component Organización https://github.com/SUI-Components

### Reutilización de código

* Contenedor-contenido 

	[diagrama de cajas]
	
* sui-component (open source)
* re, ij, mt *-Components (privados/reglas de negocio)
* "Themables" (SUIT)
  * Basic heme (npm i @schibstedspain/theme-basic)
  * re theme, ij theme, (npm i @schibstedspain/re-theme-fotocasa)
  
### Independencia de la solucion

* Frameworks volátiles
	
* Solución:
  * `npm install real-estate`
    
  * Cuando cambiemos la tecnología de UI reutilizamos todas las reglas de negocio:
    * Llamadas a otros sistemas
    * Validaciones
    * Cálculos
	  
### Problemas
* I18N (No depende de la tecnología de UI) (Rosseta)
* Tracking (Suntory)
* HTML con reglas de negocio, malo para el open source

### BTW

Usamos ReactJS para pintar el DOM




