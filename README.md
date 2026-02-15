# MCPs-Agents-And-Skills
Now that i have basics on many technologies, is time to explore how this tools can help me make my work easier. And maybe one day being a techlead or make overwork

Honestamente, no sé si haya IAS más gratuitas en las que el consumo de tokens no te limite a los aspectos de generar código.
He escuchado que si contratas claude anualmente, luego no puedes cancelarlo.

Sin embargo puesto que copilot te regala un tier para ello... y creo incluso hay maneras de conectar modelos a tu pc directo, hice una pequeña prueba...

Y los resultados si son interesantes:

<img width="1911" height="1069" alt="image" src="https://github.com/user-attachments/assets/a900bd50-934f-4119-80ff-7da9ec028a60" />

Que no haría esta cosa con un crud.... pero por los tokens no puedo ponerlo a prueba. Investigaré un poco más.
Para esto claude modifico mi readme.md principal:

````readme.md
# Calculadora - Aplicación Java

El propósito de este repositorio es crear una aplicación en Java con las 4 operaciones básicas matemáticas.

## Estructura del Proyecto

```
calculadora-app/
├── src/
│   ├── main/java/com/calculadora/
│   │   ├── Calculadora.java
│   │   └── Main.java
│   └── test/java/com/calculadora/
│       └── CalculadoraTest.java
├── pom.xml
└── README.md
```

## Requisitos

- Java 11+
- Maven 3.6+

## Compilación

```bash
mvn clean compile
```

## Ejecución

```bash
mvn exec:java -Dexec.mainClass="com.calculadora.Main"
```

## Empaquetado

```bash
mvn clean package
```

Para ejecutar el JAR generado:

```bash
java -jar target/calculadora-app-1.0-SNAPSHOT.jar
```

## Pruebas

```bash
mvn test
```

## Operaciones Disponibles

- Suma
- Resta
- Multiplicación
- División (con validación de división por cero)

## domain.md
Necesito una calculadora con las 4 operaciones matemáticas básicas.

Debe ser una aplicación normal, no spring boot, una app java normal con maven para poder
escalarlo más adelante.

Requiero comunicarme por consola con opciones para escoger que operación usar, por
cada operacion solo usar dos numeros para las operaciones y al final imprimir el resultado.

La arquitectura debe ser por capas:

-Capa de "controller": un receptor que usa una clase helper, esta clase helper implementará
el menu interactivo, y con tecla esc debo poder terminar la ejecución del programa

-Capa service: la clase que albergara el retorno de las operaciones, de preferencia con lambdas. Que
sea codigo donde se apliquen lambdas para no hacerlo muy gigantesco.
````

Solo tuve manualmente que encapsular mi codigo en un com.calculadora y listo, la única falla que le ví.
De ahí en fuera, si te ahorra bastante.....

<img width="1149" height="1078" alt="image" src="https://github.com/user-attachments/assets/784ecf4f-91cf-444e-84e7-d76bcc059d4f" />


