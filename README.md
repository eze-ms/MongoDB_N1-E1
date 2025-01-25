# Óptica Cul d'Ampolla

## 📄 Descripción
ste proyecto tiene como objetivo gestionar la información de clientes, ventas, gafas y proveedores de la óptica "Cul d'Ampolla" mediante una base de datos MongoDB. Se utiliza un enfoque basado en referencias para conectar las diferentes entidades, garantizando una estructura eficiente y escalable.

## 🗃️ Estructura de la Base de Datos

## Colecciones Principales

### 1. Clientes (Clients)
**Descripción:** Almacena la información de los clientes de la óptica.

**Campos:**
- `_id`: Identificador único del cliente (ObjectId).
- `name`: Nombre del cliente (string).
- `postal address`: Dirección postal del cliente (string).
- `phone`: Teléfono del cliente (string).
- `email`: Correo electrónico del cliente (string).
- `registerDate`: Fecha de registro del cliente (date).
- `recommendedBy`: Referencia al cliente que lo recomendó (ObjectId, opcional).

---

### 2. Ventas (Sales)
**Descripción:** Registra las ventas realizadas, conectando clientes, empleados y gafas.

**Campos:**
- `_id`: Identificador único de la venta (ObjectId).
- `client_id`: Referencia al cliente que realizó la compra (ObjectId).
- `employee_id`: Referencia al empleado que realizó la venta (ObjectId).
- `glasses_id`: Referencia a las gafas vendidas (ObjectId).
- `saleDate`: Fecha de la venta (date).
- `saleTime`: Hora de la venta (string).

---

### 3. Gafas (Glasses)
**Descripción:** Almacena la información de las gafas disponibles en la óptica.

**Campos:**
- `_id`: Identificador único de las gafas (ObjectId).
- `brand`: Marca de las gafas (string).
- `rightLensPower`: Graduación del lente derecho (double).
- `leftLensPower`: Graduación del lente izquierdo (double).
- `frameType`: Tipo de montura (string).
- `frameColor`: Color de la montura (string).
- `rightLensColor`: Color del lente derecho (string).
- `leftLensColor`: Color del lente izquierdo (string).
- `price`: Precio de las gafas (double).
- `supplier_id`: Referencia al proveedor de las gafas (ObjectId).

---

### 4. Proveedores (Suppliers)
**Descripción:** Almacena la información de los proveedores de las gafas.

**Campos:**
- `_id`: Identificador único del proveedor (ObjectId).
- `name`: Nombre del proveedor (string).
- `phone`: Teléfono del proveedor (string).


---

## 💻 Tecnologías Utilizadas
- **JSON: Formato de intercambio de datos.**
- **MongoDB: Base de datos NoSQL para almacenar la información.**
- **MongoDB Compass: Herramienta gráfica para gestionar MongoDB.**
- **Moon Modeler: Herramienta para diseñar y documentar la estructura de la base de datos.**

---

## 📊 Requisitos
- Java 11+: Para ejecutar aplicaciones que interactúen con la base de datos.
- MongoDB: Servidor de base de datos en ejecución.

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

