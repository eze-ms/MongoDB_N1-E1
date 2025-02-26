# Óptica Cul d'Ampolla

## 📝 Descripción
Este proyecto tiene como objetivo gestionar la información de clientes, compras, gafas y proveedores de la óptica "Cul d'Ampolla" mediante una base de datos MongoDB. Se utiliza un enfoque basado en documentos embebidos para conectar las diferentes entidades, facilitando la consulta y el mantenimiento de la información.

---

## 🗃️ Estructura de la Base de Datos

### Colecciones Principales

#### 1. Clientes (Clients)
**Descripción:** Almacena la información de los clientes de la óptica, incluyendo sus compras realizadas.

**Campos:**
- `_id`: Identificador único del cliente (ObjectId).
- `name`: Nombre del cliente (string).
- `address`: Dirección del cliente (string).
- `telephone`: Teléfono del cliente (string).
- `email`: Correo electrónico del cliente (string).
- `registration_date`: Fecha de registro del cliente (date).
- `shoppings`: Lista de compras realizadas por el cliente (array de documentos embebidos).

Cada compra dentro de `shoppings` contiene los siguientes campos:
- `date`: Fecha y hora de la compra (date).
- `employee`: Nombre del empleado que realizó la venta (string).
- `glasses`: Objeto con la información de las gafas adquiridas:
  - `brand`: Marca de las gafas (string).
  - `graduation`: Objeto con la graduación de cada ojo:
    - `left_eye`: Graduación del lente izquierdo (double).
    - `right_eye`: Graduación del lente derecho (double).
  - `glass_color`: Objeto con los colores de los lentes:
    - `left_eye`: Color del lente izquierdo (string).
    - `right_eye`: Color del lente derecho (string).
  - `frame_type`: Tipo de montura (string).
  - `price`: Precio de las gafas (double).
- `supplier`: Objeto con la información del proveedor:
  - `name`: Nombre del proveedor (string).
  - `address`: Dirección del proveedor (objeto con `street`, `number`, `city`, `postal_code`, `country`).
  - `phone`: Teléfono del proveedor (string).
  - `fax`: Número de fax del proveedor (string, opcional).
  - `nif`: Identificador fiscal del proveedor (string).

---

## 💻 Tecnologías Utilizadas
- **JSON:** Formato de intercambio de datos.
- **MongoDB:** Base de datos NoSQL para almacenar la información.
- **MongoDB Compass:** Herramienta gráfica para gestionar MongoDB.
- **Moon Modeler:** Herramienta para diseñar y documentar la estructura de la base de datos.

---

## 📊 Requisitos
- **Java 11+:** Para ejecutar aplicaciones que interactúen con la base de datos.
- **MongoDB:** Servidor de base de datos en ejecución.

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

