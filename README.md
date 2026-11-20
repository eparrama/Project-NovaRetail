# Project-NovaRetail  
NovaRetail+ es una plataforma de e-commerce que quiere entender qué variables de comportamiento del cliente están más asociadas con el ingreso generado  
**Herramientas utilizadas:** Python & Pandas, seaborn, matplotlib, numpy, scipy.stats: pointbiserialr & chi2_contingency  
**Datasets utilizados:** novaretail_comportamiento_clientes_2024.csv  
**Sección 1** - Cargar y explorar el dataset  
**Sección 2** - Preparar datos y documentar supuestos  
**Sección 3** - Visualización de relaciones  
**Sección 4** - Coeficientes de correlación y evidencia numérica  
Pearson / Spearman  
Punto-biserial  
V de Cramér  
**Sección 5** - Interpretación de resultados para el negocio  
**5.1 Hallazgo 1 — Relación entre Ingreso Anual vs Compras x Mes**  
La variable compras_mes sirve como un indicador del valor del cliente por lo que se deberán promover estrategias de conversión que incentiven la frecuencia de compra (programas de lealtad, ofertas por volumen o envíos gratis). Está alineado directamente con el segmento de mayor valor económico de **NovaRetail+**.  
**5.2 Hallazgo 2 — Relación entre Gasto de Publicidad Dirigida vs Visitas x Mes**  
Los datos muestran que a mayor inversión de **NovaRetail+** en anuncios dirigidos por cliente, mayor tiende a ser la frecuencia de visitas mensuales. La publicidad dirigida cumple de forma consistente su rol de atraer e incentivar el tráfico de los usuarios.  
**5.3 Hallazgo 3 —  Relación entre Ingreso Anual vs Miembro Premium**
El equipo de Crecimiento y Retención de **NovaRetail+** debe revisar los beneficios actuales del programa Premium. Si no está impulsando un valor económico superior por cliente, los incentivos actuales podrían no ser suficientes o atractivos para motivar un mayor gasto. Enfocar el presupuesto publicitario en vender membresías Premium no garantiza un incremento directo en el ingreso_anual por lo que las campañas deben centrarse en incentivar la frecuencia de compra directa (compras_mes), independientemente de la clasificación del usuario.   
**5.4 Hallazgo 4 — Relación entre Tipo Dispositivo vs Región**    
Evitar segmentar presupuestos de campañas publicitarias cruzando región con tipo de dispositivo, enfocando el esfuerzo en métricas que sí impacten el negocio.  
**Sección 6** - Limitaciones y próximos pasos  
**Limitaciones**  
- El análisis indica Correlación no Causalidad, asumir causalidad nos puede llevar a decisiones de negocio erróneas  
- Posibles efectos de segmentación no explorados  
- No se puede evaluar la estacionalidad ni la evolución del comportamiento del cliente a lo largo de varios meses al ser evaluado anualmente  
- Las compras por mes no nos dan un valor de ticket, al no contar con dicho dato no podemos saber si los miembros premium gastan más (o no) por compra no importando la frecuencia  
**Próximos pasos**  
- Dado que no se pudo establecer causalidad se recomienda implementar un A/B testing (Experimento Controlado) para superar la limitación de la correlación  
- Probar segmentación adicional:  
Con gastos de publicidad dirigida vs visitas por mes segmentado por tipo de suscripción (miembro premium)  
Ingreso Anual vs Compras x Mes segmentado por región y/o tipo de dispositivo  
Agregar la información al dataset de fechas de compra para poder establecer estacionalidad y así descartar o considerar sus efectos  
Así mismo agregar información (precio y cantidades) para obtener un valor de ticket o ingresarlo directamente para poder determinar compras por tipo de cliente en los ingresos anuales  
Para verificar el retorno de la inversión, se debe evaluar la conversión final de visitas y/o compras en ingresos.  
