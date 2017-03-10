# Patrones de Dise�o

Un patr�n de dise�o no es m�s que una �receta� que trata de proporcionar una soluci�n gen�rica a un problema concreto que se repite con frecuencia durante el desarrollo de software.

## Categor�as de patrones de dise�o

Existen una serie de categor�as para definir la funci�n que realizaba un patr�n de dise�o. A grandes rasgos, los patrones se dividen en tres grupos:

|Patrones|Descripci�n|
|---------|-----------|.
|__Creacionales__|Se trata de un conjunto de patrones cuyo objetivo es el de instanciar objeto, en lugar de recurrir a la instanciaci�n directa.|
|__Estructurales__|Definen una composici�n de objetos que, a trav�s de especializaci�n, proporcionan una funcionalidad determinada.|
|__De Comportamiento__|Se centran en c�mo interact�an e intercambian informaci�n unos objetos con otros de una manera definida.|

# Patrones de Creaci�n

Son aquellos en los que se delegaba la instanciaci�n de un objeto en otro en lugar de recurrir a un simple new().

## Builder (constructor)

Separar la construcci�n de un objeto complejo de su representaci�n, de modo que el mismo proceso de construcci�n pueda crear representaciones diferentes.

![alt tag](https://raw.githubusercontent.com/mdpl11/DesignPatterns/master/Builder/builder.png)

## Prototype

Especificar el tipo de objetos que se crear�n utilizando una instancia prototipada y crear nuevos objetos realizando copias de ese prototipo. El concepto de este patr�n es simple: en lugar de crear un objeto, se clona, es decir, se realiza una copia exacta de otro objeto dado, denominado prototipo. En .NET este proceso es sencillo, ya que nos ofrece la interfaz ICloneable que expone el m�todo Clone(), m�todo en el que habr� que codificar el proceso de copia. Ademas .NET tambi�n ofrece un m�todo, MemberwiseClone(), que autom�ticamente realiza una copia del objeto por nosotros, evit�ndonos el proceso de copiar elemento por elemento de forma manual.

![alt tag](https://raw.githubusercontent.com/mdpl11/DesignPatterns/master/Prototype/prototype.png)

#### Clonaci�n superficial y clonaci�n profunda

Cuando invocamos el m�todo MemberwiseClone() observamos que en su descripci�n indicaba que se realizaba una clonaci�n shallow o superficial. Esto significa que el clonado se realiza a nivel de bits, por lo que los objetos contenidos dentro del objeto a clonar no se clonar�n tambi�n, sino que se clonar� �nicamente la referencia del objeto. Por lo tanto, ambos objetos clonados apuntar�n al mismo objeto. Esto es lo que se conoce como clonaci�n superficial. El proceso por el cual se clonan los objetos incluidos en el objeto a clonar en lugar de copiar sus referencias se denomina clonaci�n profunda.

![alt tag](https://raw.githubusercontent.com/mdpl11/DesignPatterns/master/Prototype/ClonacionSuperficial.png)
![alt tag](https://raw.githubusercontent.com/mdpl11/DesignPatterns/master/Prototype/ClonacionProfunda.png)

# Patrones Estructurales

# Patrones de Comportamiento

## Observer

Definir una dependencia uno-a-muchos entre objetos de forma de que, cuando el estado de uno de ellos cambia, todos los objetos dependientes son notificados y actualizados de forma autom�tica.

![alt tag](https://raw.githubusercontent.com/mdpl11/DesignPatterns/master/Observer/Observer.png)

## Strategy

Definir una familia de algoritmos, encapsular cada uno de ellos y hacerlos intercambiables. Strategy permite cambiar el algoritmo independientemente de los clientes que lo utilicen.
El nombre de este patr�n evoca la posibilidad de realizar un cambio de estrategia en tiempo de ejecuci�n sustituyendo un objeto que se encargar� de implementarla.

![alt tag](https://raw.githubusercontent.com/mdpl11/DesignPatterns/master/Strategy/Strategy.png)