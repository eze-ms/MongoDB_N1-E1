# Óptica Cul d'Ampolla

## 📄 Descripción
El sistema tiene como objetivo informatizar la gestión de clientes, empleados, proveedores y ventas en la óptica "Cul d'Ampolla", utilizando MongoDB como base de datos principal y documentos embebidos para mantener una estructura ágil y eficiente.

### Características
1. **Gestión de Clientes:**
   - Almacena información del cliente: nombre, dirección (documento embebido), teléfono, email, fecha de registro y cliente recomendador `recommendedBy`.
   - Cada cliente tiene un array de ventas embebidas `sales`, que incluyen detalles de las gafas vendidas, el empleado responsable y la fecha de la venta.

2. **Gestión de Empleados:**
   - Almacena información del empleado: nombre y apellido.
   - Cada empleado tiene un array de ventas embebidas `sales`, que incluyen detalles del cliente y las gafas vendidas.

3. **Gestión de Proveedores:**
   - Almacena información del proveedor: nombre, dirección (documento embebido), teléfono, fax y NIF.
   - Cada proveedor tiene un array de gafas embebidas glasses`, que incluye detalles técnicos de las gafas, como marca, graduación, tipo y color de la montura, y precio.

4. **Gestión de Gafas:**
   - Las gafas no son una colección independiente, sino que están embebidas en las ventas y los proveedores.
   - Cada gafa almacena datos como marca, graduación de lentes, tipo y color de la montura, y precio.

5. **Gestión de Ventas:**
   - Las ventas están embebidas tanto en clientes como en empleados.
   - Incluyen detalles del cliente, las gafas vendidas, el proveedor de las gafas y el empleado que realizó la venta.

---

## 💻 Tecnologías Utilizadas
- **Java**
- **MongoDB**

---

## 📊 Requisitos
- Tener instalado **Java 11+**
- Servidor **MongoDB** en ejecución.

---

## 🛠️ Instalación
1. Clonar este repositorio:
   ```bash
   git clone https://github.com/eze-ms/MongoDB_N1-E1
   ```
2. Configurar la conexión a MongoDB en la clase correspondiente.

---

## ✨ Características Adicionales
- Validación de datos en cada inserción y actualización.
- Estructura de base de datos diseñada con Moon Modeler.
- Cumple estrictamente con el enunciado proporcionado.

---

## 📢 Notas
- Asegúrate de tener MongoDB ejecutándose en `localhost:27017`.
- Si surge algún error, revisar la conexión a la base de datos y la existencia de los documentos.

---
© 2025. Proyecto desarrollado por Ezequiel Macchi Seoane

