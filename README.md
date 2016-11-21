# Arquitectura Clean de Uncle Bob
Clean Architecture es una arquitectura que describió Uncle Bob en su blog y aunque existen otras muchas todas tienen el mismo objetivo, que es la separación de intereses o principios (separation of concerns).
Más que una arquitectura sólo son una serie de condiciones que se deben cumplir para que una arquitectura de considere ”clean”, solo son una serie de reglas que lo único que van a hacer es dividir el software en capas.
![alt text](https://github.com/OscarGovea/Clean-Uncle-Bob/blob/master/clean_archi.png)


- Entities
Son aquellos objetos que van a representar los actores importantes de la lógica de negocio de nuestra aplicación.

- Use Cases
Están muy relacionados con las entidades y son los encargados de implementar lógica de negocio de nuestra aplicación, ya que van a orientar todas aquellas interacciones del flujo de datos y entidades dejando al framework fuera de todo esto (en nuestro caso el sdk android), también se conocen como interactores.

- Interface Adapters
Convierten los datos en el formato más conveniente para los casos de uso y entidades. (De manera recurrente aqui encontraras controladores y presentadores.)

- Frameworks and Drivers
Aquí es donde residen los detalles y todo ese conjunto de plataformas externas y herramientas como puede ser la UI, Web, DB , Devices, etc. Generalmente solo se deben comunicar con el siguiente círculo a su interior.

## Android Clean Architecture
Este esquema es una representación de cómo se aplica el Clean Architecture en una aplicación android ya que gracias a la gran participación de muchos desarrolladores de la comunidad android alrededor del mundo se ha ido mejorando en estos últimos meses ya que se le han agregado dos componentes importantes el primero un patrón en la capa de presentación que puede ser MVP, MVVM, MVC o el que prefieras y el segundo se ha agregado el Repository Pattern en la capa de datos para abstraer el origen de datos y destacar que estos patrones no están dentro de la arquitectura que Uncle Bob describe, es trabajo de una comunidad con el único objetivo de mejorar el desarrollo de nuestras aplicaciones android y si estoy seguro que te encontraras diferentes implementaciones porque realmente no hay un camino a seguir pero particularmente es la que más me gusta y es la que se ha adaptado a mis problemas.
![alt text](https://github.com/OscarGovea/Clean-Uncle-Bob/blob/master/android_archi.png)

## Beneficios de Usar Arquitectura Clean
Existe una cantidad muy grande de diversas arquitecturas algunas en las cuales Uncle Bob se ha basado son Hexagonal Architecture, Onion Architecture, Screaming Architecture y lo importante es que cada una de ellas varía en sus detalles de implementación pero todas son similares y tienen el mismo objetivo separar en capas nuestro software con la finalidad de darle flexibilidad.

Las principales aportaciones que esta arquitectura seguirá motivando son:

- Independiente de frameworks
- Testable
- Independendiente de nuestra UI
- Independendiente de nuestra DB
- Independendiente de cualquier herramienta externa