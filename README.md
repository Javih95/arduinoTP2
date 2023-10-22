# arduinoTP2
examenSPD contador con numeros primos
# integrantes
Aguirre-Javier
# Proyecto: Contador binario con switch y contador Primos
![Aguirre Javier SegundaParteArduino](https://github.com/Javih95/arduinoTP2/assets/138259835/eab9e3d6-bc72-46ae-8c57-0da31899f61a)
# Descripción
Este proyecto consiste en un contador de dos dígitos que utiliza una pantalla de 7 segmentos para mostrar el valor del contador. Los botones "SUBE", "BAJA" y "Interruptor" permiten incrementar, disminuir y cambiar el contador para mostrar numeros primos respectivamente.
# Función principal
monitorea constantemente si se han presionado los botones "SUBE", "BAJA" o "Interruptor", y toma acciones en función de los botones presionados, como incrementar, disminuir o cambiar la funcion a mostrar en los displays. Además, se encarga de mostrar el valor del contador en los Displays de 7 segmentos.
void loop()
{
  int estadoInterruptor = digitalRead(interruptor);
  if (estadoInterruptor == LOW) 
  {
    PrintCount();// Muestra el valor del contador en el Display
    int presionado = KeyPressed();// Detecta si se ha presionado uno de los botones
    if(presionado == 	SUBE)
    {
      sumar();
    }
    if(presionado == BAJA)
    {
      restar();
    }
  
  }
  else if (estadoInterruptor == HIGH)
  {
    PrintNumeroPrimo();// Muestra el valor del contador en el Display solo si es un numero Primo
    int presionado = KeyPressed();// Detecta si se ha presionado uno de los botones
    if(presionado == 	SUBE)
    {
      sumar();
    }
  }
}
# Enlace al proyecto
https://www.tinkercad.com/things/3lFp4HN0W1S
