# Instrucciones para replicar el caso práctico

A continuación, se presenta una guía detallada y práctica para desarrollar y ejecutar una estrategia de trading utilizando ChatGPT y TradingView. Esta guía está diseñada para ser fácil de seguir, incluso para principiantes en el mundo del trading.

<div align="justify">
   
# Paso 1: Configurar el indicador en TradingView y copiar el código en el Editor Pine
   
1. **Abrir TradingView y cargar el gráfico del activo:**
   
   - Visita [TradingView](https://www.tradingview.com) y crea una cuenta o inicia sesión si ya tienes una.
     
   ![alt text](https://github.com/franmandres/GPT-for-trading-analysis/blob/main/imagenes/capturas/Capture1.png "Capture1")
   
   - En la barra de búsqueda en la parte superior de la página, escribe el par de activos que te interesa, por ejemplo, "BTC/EUR" (el cual hace referencia a la variación del precio del Bitcoin en la divisa euro) y selecciona el gráfico correspondiente de la lista desplegable. Como recomendación, en estos casos donde se dispone de muchos spots de donde elegir mostrar gráfico, es conveniente escoger el más grande o conocido pues estará más actualizado, por ello elegimos BINANCE.
     
   ![alt text](https://github.com/franmandres/GPT-for-trading-analysis/blob/main/imagenes/capturas/Capture2.png "Capture2")
   
   - Una vez abierto el grafico, tendría que salirnos algo similar a la imagen que se muestra a continuación. Es importante fijarnos en la esquina superior izquierda y asegurarse de que se nos muestra el gráfico Bitcoin/Euro × 1D × BINANCE.
     
   ![alt text](https://github.com/franmandres/GPT-for-trading-analysis/blob/main/imagenes/capturas/Capture3.png "Capture3")   
3. **Añadir el indicador técnico:**
   
   - En la barra superior del gráfico, haz clic en el icono de "Indicadores" (representado por un gráfico de líneas con un símbolo de suma).
     
   ![alt text](https://github.com/franmandres/GPT-for-trading-analysis/blob/main/imagenes/capturas/Capture4.png "Capture4")  
   - En la barra de búsqueda de indicadores que aparece, escribe "Supertrend" y selecciónalo para añadirlo a tu gráfico. El Supertrend es un indicador de tendencia basado en el Average True Range (ATR). Este indicador de línea única combina la detección de tendencias y la volatilidad, permitiendo anticipar cambios en la dirección de la tendencia y establecer niveles de stop-loss efectivos.
     
   ![alt text](https://github.com/franmandres/GPT-for-trading-analysis/blob/main/imagenes/capturas/Capture5.png "Capture5")
    
   - Así quedaría el grafico una vez se selecciona el indicador.
     
   ![alt text](https://github.com/franmandres/GPT-for-trading-analysis/blob/main/imagenes/capturas/Capture6.png "Capture6")
   
   - Podemos obtener más información sobre el indicador "Supertrend" colocando el cursor sobre su nombre en el lado izquierdo del gráfico, haciendo clic en los tres puntos (opción "Más"), y seleccionando "Acerca de este script".
     
   ![alt text](https://github.com/franmandres/GPT-for-trading-analysis/blob/main/imagenes/capturas/Capture7.png "Capture7")
   
   - Esto abrirá una ventana en el lado derecho que proporciona detalles sobre el indicador, incluyendo su descripción, historia y método de cálculo.
   
   ![alt text](https://github.com/franmandres/GPT-for-trading-analysis/blob/main/imagenes/capturas/Capture8.png "Capture8")

5. **Abrir el código fuente del indicador:**
   
   - Con el indicador Supertrend visible en el gráfico, haz clic derecho sobre el nombre del indicador en la lista de indicadores situada en la parte izquierda del gráfico. Selecciona "Código fuente" para abrir el código del indicador en el Editor Pine.
     
   ![alt text](https://github.com/franmandres/GPT-for-trading-analysis/blob/main/imagenes/capturas/Capture9.png "Capture9")
   
   - Otra forma de abrirlo es seleccionando directamente sobre el icono de { } situado al lado del nombre del indicador.
     
   ![alt text](https://github.com/franmandres/GPT-for-trading-analysis/blob/main/imagenes/capturas/Capture10.png "Capture10")
   
   - El Editor Pine se abrirá mostrando el código en lenguaje Pine Script. Si no ves la ventana del editor de inmediato, es posible que esté minimizada en la parte inferior de la pantalla según la configuración de tu vista. Simplemente arrastra la ventana hacia arriba para verla con claridad. Luego, copia todo el código que se muestra en el editor.
   
   ![alt text](https://github.com/franmandres/GPT-for-trading-analysis/blob/main/imagenes/capturas/Capture11.png "Capture11")

# Paso 2: Solicitar a ChatGPT que genere una estrategia de trading

1. **Pegar el código del indicador en ChatGPT:**
   
   - Abre ChatGPT e inicia una nueva conversación. Pega el código del indicador Supertrend que copiaste previamente en el cuadro de texto de ChatGPT.
  
   ![alt text](https://github.com/franmandres/GPT-for-trading-analysis/blob/main/imagenes/capturas/Capture12.png "Capture12")

3. **Solicitar la estrategia de trading:**
   
   - Formula la solicitud para generar una estrategia específica. Por ejemplo:
*"¿Podrías usar el código que te acabo de pasar para generar una estrategia en Pine Script que compre cuando el indicador Supertrend rompa de abajo hacia arriba el precio de BTC/EUR, y venda cuando rompa el mismo precio de arriba hacia abajo?"*

   ![alt text](https://github.com/franmandres/GPT-for-trading-analysis/blob/main/imagenes/capturas/Capture13.png "Capture13")

   - ChatGPT procesará la solicitud y generará el código Pine Script correspondiente para la estrategia de compra y venta basada en el indicador Supertrend.
  
   ![alt text](https://github.com/franmandres/GPT-for-trading-analysis/blob/main/imagenes/capturas/Capture14.png "Capture14")
   ![alt text](https://github.com/franmandres/GPT-for-trading-analysis/blob/main/imagenes/capturas/Capture15.png "Capture15")

# Paso 3: Introducir el nuevo código en el Editor Pine de TradingView

1. **Volver a TradingView y abrir el Editor Pine:**
   
   - Regresa a TradingView y abre el Editor Pine.

   ![alt text](https://github.com/franmandres/GPT-for-trading-analysis/blob/main/imagenes/capturas/Capture16.png "Capture16")

2. **Crear una copia del script original:**
   
   - En el Editor Pine, crea una copia del script original haciendo clic en "Guardar como" y dando un nuevo nombre al script.
  
   ![alt text](https://github.com/franmandres/GPT-for-trading-analysis/blob/main/imagenes/capturas/Capture17.png "Capture17")

   - Lo vamos a llamar, por ejemplo, "Supertrend BTC/EUR Strategy". De esta manera el mensaje de “Este script es de solo lectura” desaparece y podemos modificar el código.
  
   ![alt text](https://github.com/franmandres/GPT-for-trading-analysis/blob/main/imagenes/capturas/Capture18.png "Capture18")

3. **Reemplazar el código antiguo:**
   
   - Borra todo el código antiguo en el Editor Pine. Pega el nuevo código generado por ChatGPT.

   ![alt text](https://github.com/franmandres/GPT-for-trading-analysis/blob/main/imagenes/capturas/Capture19.png "Capture19")

4. **Guardar y aplicar el script:**
   
   - Haz clic en "Guardar" para guardar el nuevo script. Luego, haz clic en "Añadir al gráfico" para aplicar el script al gráfico de Bitcoin/EUR.
  
   ![alt text](https://github.com/franmandres/GPT-for-trading-analysis/blob/main/imagenes/capturas/Capture20.png "Capture20")

   - Así es como quedaría el gráfico una vez hayamos añadido nuestro script con la estrategia, donde se nos crean los indicadores de compra y venta con diferentes colores.
  
   ![alt text](https://github.com/franmandres/GPT-for-trading-analysis/blob/main/imagenes/capturas/Capture21.png "Capture21")

# Paso 4: Realizar la gestión de riesgos

1. **Ajustar la configuración de la estrategia:**

   - Haz clic en la rueda de configuración del script en el gráfico para abrir la ventana de propiedades.

   ![alt text](https://github.com/franmandres/GPT-for-trading-analysis/blob/main/imagenes/capturas/Capture22.png "Capture22")

2. **Configurar parámetros de gestión de riesgos:**

   - **Capital inicial:** Configura el capital inicial que deseas utilizar (por ejemplo, 150.000€).
   - **Divisa de referencia:** Establece la divisa de referencia (por ejemplo, euros).
   - **Tamaño de la orden:** Define el tamaño de la orden como un porcentaje del patrimonio (por ejemplo, 5%).
   - **Efecto pirámide:** Establece el efecto pirámide en 1.
   - **Comisión:** Configura la comisión por orden (por ejemplo, 1 euro/orden).
   - **Margen para posiciones largas:** Es el capital que un inversor debe depositar como garantía para abrir y mantener una posición larga en el mercado. Establecemos como margen 1.
   - **Margen para posiciones cortas:** Es el capital que un inversor debe depositar como garantía para abrir y mantener una posición corta en el mercado. Establecemos como margen 2.
   - **Recalcular:** Seleccionamos que se recalcule la estrategia una vez ejecutada la orden.

   ![alt text](https://github.com/franmandres/GPT-for-trading-analysis/blob/main/imagenes/capturas/Capture23.png "Capture23")

3. **Recalcular resultados:**

   - Haz clic en "Recalcular" para actualizar los resultados de la estrategia considerando las nuevas configuraciones de gestión de riesgos. Revisa los resultados ajustados para ver la rentabilidad real de la estrategia.
     
## Paso 5: Establecer alertas

1. **Configurar alertas en TradingView:**

   - Haz clic en el icono de reloj (Alertas) en la parte superior derecha de TradingView para abrir la ventana de alertas.
  
   ![alt text](https://github.com/franmandres/GPT-for-trading-analysis/blob/main/imagenes/capturas/Capture24.png "Capture24")

2. **Establecer la condición de la alerta:**

   - Selecciona el script que guardaste, "Supertrend BTC/EUR Strategy". Configura la condición de la alerta para que se active cuando se cumplan los criterios de compra o venta definidos en la estrategia.

3. **Definir el vencimiento de las alertas:**

   - Establece el vencimiento de las alertas al máximo posible para no tener que renovarlas frecuentemente.

4. **Guardar la configuración de alertas:**

   - Dale un nombre a la alerta, como "Alerta Supertrend". Haz clic en "Guardar" para activar la alerta.
  
      ![alt text](https://github.com/franmandres/GPT-for-trading-analysis/blob/main/imagenes/capturas/Capture25.png "Capture25")

5. **Monitorear y ajustar:**

   - Monitorea las alertas y ajusta la estrategia según las condiciones del mercado y el análisis continuo.
