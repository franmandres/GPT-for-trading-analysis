# Instrucciones para replicar el caso práctico

A continuación, se presenta una guía detallada y práctica para desarrollar y ejecutar una estrategia de trading utilizando ChatGPT y TradingView. Esta guía está diseñada para ser fácil de seguir, incluso para principiantes en el mundo del trading.

<div align="justify">
   
# Paso 1: Configurar el indicador en TradingView y copiar el código en el Editor Pine
   
1. **Abrir TradingView y cargar el gráfico del activo:**
   
   - Visita [TradingView](https://www.tradingview.com) y crea una cuenta o inicia sesión si ya tienes una.
   ![alt text](https://github.com/franmandres/GPT-for-trading-analysis/blob/main/images/instructions captures/Capture1.png "Capture1")

   - En la barra de búsqueda, escribe el par de activos que te interesa, por ejemplo, "BTC/EUR" (precio de Bitcoin en euros), y selecciona el gráfico correspondiente. Se recomienda elegir el gráfico de un mercado grande como BINANCE para asegurar datos actualizados.
   ![alt text](https://github.com/franmandres/GPT-for-trading-analysis/blob/main/images/instructions captures/Capture1.png "Capture1")
   - Asegúrate de que el gráfico seleccionado muestre "Bitcoin/Euro × 1D × BINANCE" en la esquina superior izquierda.

3. **Añadir el indicador técnico:**
   
   - Haz clic en el icono de "Indicadores" (representado por un gráfico de líneas con un símbolo de suma) en la barra superior del gráfico.
   - Busca "Supertrend" en la barra de búsqueda de indicadores y selecciónalo para añadirlo al gráfico. Este indicador ayuda a detectar tendencias y volatilidad, estableciendo niveles efectivos de stop-loss.
   - Para obtener más información sobre "Supertrend", coloca el cursor sobre su nombre en el lado izquierdo del gráfico, haz clic en los tres puntos (opción "Más"), y selecciona "Acerca de este script".

4. **Abrir el código fuente del indicador:**
   
   - Haz clic derecho sobre el nombre del indicador en la lista de indicadores a la izquierda del gráfico y selecciona "Código fuente" para abrir el código en el Editor Pine.
   - Alternativamente, puedes hacer clic en el icono de { } junto al nombre del indicador.
   - Copia todo el código que se muestra en el Editor Pine. Si la ventana del editor está minimizada, arrástrala hacia arriba para verla claramente.

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
