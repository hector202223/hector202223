# **Ejemplo Completo: Hoja Panel (Dashboard) en Google Sheets**

Aquí te muestro cómo debería verse tu **hoja Panel** con datos reales basados en tus imágenes, incluyendo gráficos, métricas y tablas resumen:

---

## **📊 DASHBOARD DE VENTAS**  
*(Total actualizado automáticamente desde la hoja "Datos")*  

### **📌 Métricas Clave**  
| Concepto          | Valor ($)   | Fórmula en Google Sheets           |
|-------------------|-------------|------------------------------------|
| **Venta Total**   | **23,300**  | `=SUM(Datos!D2:D5)`                |
| **Menor Venta**   | **3,500**   | `=MIN(Datos!D2:D5)`                |
| **Mayor Venta**   | **8,500**   | `=MAX(Datos!D2:D5)`                |
| **Promedio**      | **5,825**   | `=AVERAGE(Datos!D2:D5)`            |
| **Mejor Tienda**  | **Tienda2** | `=IF(SUM(Datos!B2:B5)>SUM(Datos!C2:C5),"Tienda1","Tienda2")` |

---

### **📈 Gráficos (Referenciados desde "Datos")**  

#### **1. Ventas por Semana (Barras Agrupadas)**  
![Gráfico de Barras]  
*(Configuración: Datos = `'Datos'!A1:C5`, Tipo = "Barras agrupadas")*  

#### **2. Evolución de Venta Total (Líneas)**  
![Gráfico de Líneas]  
*(Configuración: Datos = `'Datos'!A1:A5` y `'Datos'!D1:D5`, Tipo = "Líneas")*  

---

### **📋 Tabla Resumen Semanal**  

| **Semana** | **Tienda1 ($)** | **Tienda2 ($)** | **Total ($)** | **% Tienda1** | **% Tienda2** |
|------------|-----------------|-----------------|---------------|---------------|---------------|
| Semana 1   | 2,000           | 1,500           | **3,500**     | 57.1%         | 42.9%         |
| Semana 2   | 3,500           | 2,500           | **6,000**     | 58.3%         | 41.7%         |
| Semana 3   | 1,800           | 3,500           | **5,300**     | 34.0%         | 66.0%         |
| Semana 4   | 4,000           | 4,500           | **8,500**     | 47.1%         | 52.9%         |

*(Fórmulas usadas: `=B2+C2` para Total, `=B2/D2` para % Tienda1, etc.)*  

---

### **🔹 Consejos Finales**  
✅ **Oculta la hoja "Datos"** (clic derecho → Ocultar) para que solo se vea el Panel.  
✅ **Usa formato condicional** para resaltar semanas con mejor desempeño.  
✅ **Actualiza automáticamente**: Si modificas "Datos", el Panel se recalcula solo.  

---

### **📌 ¿Cómo se vería en Google Sheets?**  
(Así debería verse tu Dashboard terminado)  

![Ejemplo visual de un dashboard organizado con métricas, gráficos y tabla resumen]  

---

### **🔄 ¿Qué pasa si actualizo los datos?**  
Si en la hoja "Datos" cambias:  
- **Semana 1 / Tienda1 = 2,500 → El Panel actualizará:**  
  - Venta Total: **23,800** (antes 23,300)  
  - % Tienda1 en Semana 1: **62.5%** (antes 57.1%)  
  - Gráficos se ajustan automáticamente.  

---

Con esta estructura, tu Dashboard será **claro, profesional y totalmente dinámico**. ¿Necesitas ayuda para implementarlo paso a paso? 😊