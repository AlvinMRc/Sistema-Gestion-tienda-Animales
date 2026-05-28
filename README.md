🐾 Paw House System
Sistema de gestión de escritorio para tiendas especializadas en la venta de animales (pet shops), desarrollado en Java Swing con base de datos MySQL.

📋 Descripción
Paw House System centraliza la administración de una tienda de animales, permitiendo gestionar empleados, inventario de animales, órdenes de compra, ventas y proveedores desde una sola plataforma. Reemplaza el manejo manual de información por un entorno digital seguro y organizado.

 Módulos del Sistema
MóduloDescripciónLoginAutenticación de usuario con tema oscuro FlatLafDashboardPanel principal con métricas (clientes, ventas, mascotas, citas)AnimalesInventario de animales: categoría, raza, género, color, precioÓrdenes de CompraRegistro de órdenes a suplidores con costo de envíoÍtems de OrdenDetalle de animales incluidos por ordenEmpleadosGestión de personal con jerarquía y datos de contactoVentasRegistro de ventas vinculadas a clientes y empleadosInventario Prod.Productos (alimentos, accesorios, medicinas) con control de stockProveedoresRegistro de suplidores con datos de contactoAyudaCentro de ayuda con instrucciones de uso

 Tecnologías

Java 25 — Lenguaje principal
Java Swing — Interfaz gráfica de usuario
FlatLaf 3.6 — Tema visual Dark moderno
MySQL 8.0+ — Base de datos relacional
Laragon 6.0+ — Servidor local MySQL
JDBC (mysql-connector-j 8.3.0) — Conexión Java ↔ MySQL
Apache Maven 3.x — Gestión de dependencias


 Requisitos

Java JDK 21 o superior
Apache Maven 3.x
Laragon (o cualquier servidor MySQL local) en el puerto 3306
Base de datos paw_house_db creada en MySQL


 Base de Datos
La base de datos se llama paw_house_db. Las tablas principales son:
clientes · Employee · Animal · AnimalOrder · AnimalOrderItem · Sale · SaleAnimal
La conexión se configura en src/main/java/com/pawhouse/system/config/DatabaseConnection.java.

 Instalación y Ejecución
bash# 1. Clonar el repositorio
git clone https://github.com/AlvinMRc/Sistema-Gestion-tienda-Animales.git

# 2. Importar la base de datos en MySQL (con Laragon activo)
#    Crear la base de datos: paw_house_db

# 3. Compilar y ejecutar con Maven
mvn clean install
mvn exec:java

👥 Roles de Usuario
FunciónAdminEmpleadoRegistrar / Actualizar / Eliminar, Buscar y visualizar información. Gestionar proveedores y empleados. Acceder a reportes.

 Estructura del Proyecto
com.pawhouse.system
├── config/       # DatabaseConnection.java
├── models/       # POJOs (Animal, Employee, Sale, ...)
├── dao/          # Operaciones SQL (AnimalDAO, SaleDAO, ...)
└── views/        # Formularios Swing (Login, Dashboard, Paneles)

Soporte
pawhouse@gmail.com
