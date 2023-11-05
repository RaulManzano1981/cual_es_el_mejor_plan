# cual_es_el_mejor_plan
Se va a realizar un análisis preliminar de las tarifas basado en una selección de clientes relativamente pequeña. Tendrás los datos de 500 clientes de Megaline: quiénes son los clientes, de dónde son, qué tarifa usan, así como la cantidad de llamadas que hicieron y los mensajes de texto que enviaron en 2018. Tu trabajo es analizar el comportamiento de los clientes y determinar qué tarifa de prepago genera más ingresos.

Durante este proyecto se buscará determinar que plan genera más ingresos para la empresa, para ello se preprocesaran los datos, se utilizaran herramientas estadisticas, tales como histogramas, gráficos de caja para visualizar si hay consumos atipicos por parte de los usuarios en llamadas, mensajes y en la navegación con datos.

También se realizarán pruebas de hipótesis para los siguientes supuestos:

El ingreso promedio para ambos planes es diferente

el ingreso promedio de los usuarios del área de NY-NJ es diferente a los de las otras regiones

Para ello se realizarán ttest, se buscará el valor de la varianza, que ayudaran a descartar o no las hipótesis anteriormente planteadas.

Los datasets a utilizar son los siguientes:

#### calls_info = pd.read_csv("/datasets/megaline_calls.csv")
* id         identificación de llamada 
* user_id    Número de usuario 
* call_date  Fecha de la llamada 
* duration   Duración de la llamda

#### internet_info = pd.read_csv("/datasets/megaline_internet.csv")
*id            identificación de conexión
*user_id       Número de usuario  
*session_date  Fecha de conexión
*mb_used       Megas utilizados

#### message_info = pd.read_csv("/datasets/megaline_messages.csv")
* id            Identificación del mesaje
* user_id       Número de usario 
* message_date  Fecha del mensaje

#### plans_info = pd.read_csv("/datasets/megaline_plans.csv")
* messages_included      Mensajes incluidos 
* mb_per_month_included  Gigas de navecación 
* minutes_included       Minutos de llamadas 
* usd_monthly_pay        Tarifa  
* usd_per_gb             Costo del giga adicional
* usd_per_message        costo de mensajes adicionales
* usd_per_minute         Costo minutos adicionales
* plan_name              Nombre del plan

#### users_info = pd.read_csv("/datasets/megaline_users.csv")
* user_id     Número de usuario
* first_name  Primer nombre
* last_name   Primer apellido
* age         Edad
* city        Ciudad
* reg_date    Fecha de registro
* plan        Plan registrado
* churn_date  Fecha de desafiliación del plan
