# Instrucciones para replicar el caso práctico

A continuación, se presenta una guía detallada y práctica para desarrollar y ejecutar una estrategia de trading utilizando ChatGPT y TradingView. Esta guía está diseñada para ser fácil de seguir, incluso para principiantes en el mundo del trading.

<div align="justify">
   
# Paso 1: Configurar el indicador en TradingView y copiar el código en el Editor Pine
   
1. **Abrir TradingView y cargar el gráfico del activo:**
   
   - Visita [TradingView](https://www.tradingview.com) y crea una cuenta o inicia sesión si ya tienes una.
   
   ![alt text](https://github.com/franmandres/GPT-for-trading-analysis/blob/main/images/instructionscaptures/Capture1.png "Capture1")
   
   - En la barra de búsqueda en la parte superior de la página, escribe el par de activos que te interesa, por ejemplo, "BTC/EUR" (el cual hace referencia a la variación del precio del Bitcoin en la divisa euro) y selecciona el gráfico correspondiente de la lista desplegable. Como recomendación, en estos casos donde se dispone de muchos spots de donde elegir mostrar gráfico, es conveniente escoger el más grande o conocido pues estará más actualizado, por ello elegimos BINANCE.
   ![alt text](https://github.com/franmandres/GPT-for-trading-analysis/blob/main/images/instructionscaptures/Capture2.png "Capture2")
   - Una vez abierto el grafico, tendría que salirnos algo similar a la imagen que se muestra a continuación. Es importante fijarnos en la esquina superior izquierda y asegurarse de que se nos muestra el gráfico Bitcoin/Euro × 1D × BINANCE.
   ![alt text](https://github.com/franmandres/GPT-for-trading-analysis/blob/main/images/instructionscaptures/Capture3.png "Capture3")   

3. **Añadir el indicador técnico:**
   
   - En la barra superior del gráfico, haz clic en el icono de "Indicadores" (representado por un gráfico de líneas con un símbolo de suma).
   ![alt text](https://github.com/franmandres/GPT-for-trading-analysis/blob/main/images/instructionscaptures/Capture4.png "Capture4")  
   - En la barra de búsqueda de indicadores que aparece, escribe "Supertrend" y selecciónalo para añadirlo a tu gráfico. El Supertrend es un indicador de tendencia basado en el Average True Range (ATR). Este indicador de línea única combina la detección de tendencias y la volatilidad, permitiendo anticipar cambios en la dirección de la tendencia y establecer niveles de stop-loss efectivos.
   ![alt text](https://github.com/franmandres/GPT-for-trading-analysis/blob/main/images/instructionscaptures/Capture5.png "Capture5") 
   - Así quedaría el grafico una vez se selecciona el indicador.
   ![alt text](https://github.com/franmandres/GPT-for-trading-analysis/blob/main/images/instructionscaptures/Capture6.png "Capture6")
   - Podemos obtener más información sobre el indicador "Supertrend" colocando el cursor sobre su nombre en el lado izquierdo del gráfico, haciendo clic en los tres puntos (opción "Más"), y seleccionando "Acerca de este script".
   ![alt text](https://github.com/franmandres/GPT-for-trading-analysis/blob/main/images/instructionscaptures/Capture7.png "Capture7")
   - Esto abrirá una ventana en el lado derecho que proporciona detalles sobre el indicador, incluyendo su descripción, historia y método de cálculo.
   ![alt text](https://github.com/franmandres/GPT-for-trading-analysis/blob/main/images/instructionscaptures/Capture8.png "Capture8")

4. **Abrir el código fuente del indicador:**
   
   - Con el indicador Supertrend visible en el gráfico, haz clic derecho sobre el nombre del indicador en la lista de indicadores situada en la parte izquierda del gráfico. Selecciona "Código fuente" para abrir el código del indicador en el Editor Pine.
   ![alt text](https://github.com/franmandres/GPT-for-trading-analysis/blob/main/images/instructionscaptures/Capture9.png "Capture9")
   - Otra forma de abrirlo es seleccionando directamente sobre el icono de { } situado al lado del nombre del indicador.
   ![alt text](https://github.com/franmandres/GPT-for-trading-analysis/blob/main/images/instructionscaptures/Capture10.png "Capture10")
   - El Editor Pine se abrirá mostrando el código en lenguaje Pine Script. Si no ves la ventana del editor de inmediato, es posible que esté minimizada en la parte inferior de la pantalla según la configuración de tu vista. Simplemente arrastra la ventana hacia arriba para verla con claridad. Luego, copia todo el código que se muestra en el editor.
   ![alt text](https://github.com/franmandres/GPT-for-trading-analysis/blob/main/images/instructionscaptures/Capture11.png "Capture11")

# Paso 2: Solicitar a ChatGPT que genere una estrategia de trading

1. **Pegar el código del indicador en ChatGPT:**
   
   - Abre ChatGPT e inicia una nueva conversación. Pega el código del indicador Supertrend en el cuadro de texto de ChatGPT.

3. **Solicitar la estrategia de trading:**
   
   - Formula una solicitud específica, como: "¿Podrías usar el código que te acabo de pasar para generar una estrategia en Pine Script que compre cuando el indicador Supertrend rompa de abajo hacia arriba el precio de BTC/EUR, y venda cuando rompa el mismo precio de arriba hacia abajo?"
   - ChatGPT generará el código Pine Script para la estrategia basada en el indicador Supertrend.

# Paso 3: Introducir el nuevo código en el Editor Pine de TradingView

1. **Volver a TradingView y abrir el Editor Pine:**
   
   - Regresa a TradingView y abre el Editor Pine.

3. **Crear una copia del script original:**
   
   - En el Editor Pine, haz clic en "Guardar como" y nombra el script, por ejemplo, "Supertrend BTC/EUR Strategy". Esto permite modificar el script.

5. **Reemplazar el código antiguo:**
   
   - Borra el código antiguo y pega el nuevo código generado por ChatGPT.

7. **Guardar y aplicar el script:**
   
   - Haz clic en "Guardar" y luego en "Añadir al gráfico" para aplicar el script al gráfico de Bitcoin/EUR.

# Paso 4: Realizar la gestión de riesgos

1. **Ajustar la configuración de la estrategia:**

   - Haz clic en la rueda de configuración del script en el gráfico para abrir la ventana de propiedades.

2. **Configurar parámetros de gestión de riesgos:**

   - **Capital inicial:** Configura el capital inicial (ej. 150.000€).
   - **Divisa de referencia:** Establece la divisa de referencia (ej. euros).
   - **Tamaño de la orden:** Define el tamaño de la orden como un porcentaje del patrimonio (ej. 5%).
   - **Efecto pirámide:** Establece el efecto pirámide en 1.
   - **Comisión:** Configura la comisión por orden (ej. 1 euro/orden).
   - **Margen para posiciones largas:** Establece el margen (ej. 1).
   - **Margen para posiciones cortas:** Establece el margen (ej. 2).
   - **Recalcular:** Selecciona la opción para recalcular la estrategia una vez ejecutada la orden.

3. **Recalcular resultados:**

   - Haz clic en "Recalcular" para actualizar los resultados de la estrategia con las nuevas configuraciones de gestión de riesgos.

## Paso 5: Establecer alertas

1. **Configurar alertas en TradingView:**

   - Haz clic en el icono de reloj (Alertas) en la parte superior derecha de TradingView.

2. **Establecer la condición de la alerta:**

   - Selecciona el script guardado, "Supertrend BTC/EUR Strategy", y configura la condición para activar la alerta cuando se cumplan los criterios de compra o venta.

3. **Definir el vencimiento de las alertas:**

   - Establece el vencimiento de las alertas al máximo posible para evitar renovarlas frecuentemente.

4. **Guardar la configuración de alertas:**

   - Dale un nombre a la alerta, como "Alerta Supertrend", y haz clic en "Guardar".

5. **Monitorear y ajustar:**

   - Monitorea las alertas y ajusta la estrategia según las condiciones del mercado y el análisis continuo.
