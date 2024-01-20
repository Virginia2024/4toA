-- Tabla Usuario
CREATE TABLE Usuario (
ID INT PRIMARY KEY AUTO_INCREMENT,
Nombre VARCHAR(255),
Email VARCHAR(255),
Contraseña VARCHAR(255),
TipoUsuario ENUM(&#39;Vendedor&#39;, &#39;Comprador&#39;)
);

-- Tabla Producto
CREATE TABLE Producto (
ID INT PRIMARY KEY AUTO_INCREMENT,

Nombre VARCHAR(255),
Descripcion TEXT,
Precio DECIMAL(10, 2),
CantidadDisponible INT,
VendedorID INT,
CategoriaProductoID INT
);

-- Tabla CategoriaProducto
CREATE TABLE CategoriaProducto (
ID INT PRIMARY KEY AUTO_INCREMENT,
Nombre VARCHAR(255)
);

-- Tabla CompraProducto
CREATE TABLE CompraProducto (
ID INT PRIMARY KEY AUTO_INCREMENT,
CompradorID INT,
ProductoID INT,
Cantidad INT,
FechaCompra DATETIME
);

-- Tabla ImagenProducto
CREATE TABLE ImagenProducto (
ID INT PRIMARY KEY AUTO_INCREMENT,
ProductoID INT,
URLImagen VARCHAR(255)
);

-- Tabla ComentarioProducto
CREATE TABLE ComentarioProducto (

ID INT PRIMARY KEY AUTO_INCREMENT,
ProductoID INT,
CompradorID INT,
Comentario TEXT,
Calificacion INT
);
