# 📦 Sistema de Inventario Pro - Demo Funcional

![Estado](https://img.shields.io/badge/Estado-Demo_Activo-success)
![Versión](https://img.shields.io/badge/Versión-1.0-blue)
![Licencia](https://img.shields.io/badge/Licencia-MIT-green)

> Sistema empresarial completo de gestión de inventario con dashboard interactivo, analytics en tiempo real y funcionalidades CRUD avanzadas.

## 🌐 **Demo en Vivo**

**🚀 [Ver Demo en Vivo](https://inventario-demo.netlify.app/)**

**🔗 URLs de Demo:**
- Netlify: https://inventario-demo.netlify.app/
- GitHub Pages: https://projectone2020.github.io/sistema-inventario-demo/

---

## ✨ **Características Principales**

### 🔐 **Sistema de Autenticación Dual**
- **Superadmin**: Control total del sistema
  - Usuario: `admin` / Contraseña: `admin123`
- **Viewer**: Vista de solo lectura
  - Usuario: `viewer` / Contraseña: `viewer123`

### 📊 **Dashboard Interactivo**
- Analytics en tiempo real
- Gráficos visuales de inventario
- Alertas de stock bajo
- Estadísticas por categoría
- Métricas de valor total

### 🗂️ **Gestión Completa CRUD**
- ➕ Crear productos
- ✏️ Editar productos existentes
- 🗑️ Eliminar productos (con confirmación)
- 🔍 Búsqueda en tiempo real
- 🏷️ Filtrado por categorías
- 📈 Ordenamiento múltiple (nombre, precio, stock)

### 📝 **Sistema de Auditoría**
- Registro completo de cambios
- Historial de acciones (últimas 50)
- Tracking por usuario y timestamp
- Vista de actividad reciente

### 📥📤 **Import/Export**
- Exportar inventario a CSV
- Importar productos desde CSV
- Formato compatible con Excel
- Respaldo de datos

### 🎨 **Interfaz Moderna**
- Diseño responsive (mobile-first)
- Animaciones suaves
- Dark mode friendly
- UX intuitiva
- Componentes accesibles

---

## 🛠️ **Tecnologías Utilizadas**

### **Frontend**
- **React 18** - Framework principal
- **JavaScript ES6+** - Lógica de aplicación
- **Tailwind CSS** - Estilos y diseño
- **Lucide React** - Iconografía

### **Almacenamiento**
- **LocalStorage** - Persistencia de datos
- **Session Management** - Control de usuarios

### **Deployment**
- **Netlify** - Hosting principal
- **GitHub Pages** - Mirror de respaldo

---

## 🚀 **Instalación y Uso**

### **Opción 1: Demo en Línea (Recomendado)**

Simplemente visita: [https://inventario-demo.netlify.app/](https://inventario-demo.netlify.app/)

### **Opción 2: Ejecutar Localmente**

```bash
# 1. Clonar el repositorio
git clone https://github.com/projectone2020/sistema-inventario-demo.git

# 2. Navegar al directorio
cd sistema-inventario-demo

# 3. Abrir index.html en tu navegador
# Opción A: Doble click en index.html
# Opción B: Usar un servidor local
python -m http.server 8000
# Luego visita: http://localhost:8000
```

### **Credenciales de Acceso**

#### **Superadmin** (Control Total)
```
Usuario: admin
Contraseña: admin123
```

#### **Viewer** (Solo Lectura)
```
Usuario: viewer
Contraseña: viewer123
```

---

## 📋 **Funcionalidades por Rol**

### **Superadmin** ✅
- ✅ Ver dashboard completo
- ✅ Crear productos
- ✅ Editar productos
- ✅ Eliminar productos
- ✅ Exportar datos
- ✅ Importar datos
- ✅ Ver historial completo

### **Viewer** 👁️
- ✅ Ver dashboard
- ✅ Buscar productos
- ✅ Filtrar por categoría
- ✅ Ver detalles de productos
- ✅ Exportar datos (solo lectura)
- ❌ No puede crear/editar/eliminar

---

## 📊 **Datos de Ejemplo**

El sistema viene precargado con 12 productos de ejemplo en las siguientes categorías:

- 📱 **Electrónica** (Laptops, Monitores, Tablets)
- 🖱️ **Accesorios** (Mouse, Teclados, Webcams)
- 🎧 **Audio** (Auriculares)
- 💾 **Almacenamiento** (SSDs)
- 🔧 **Componentes** (Memoria RAM)
- 🌐 **Redes** (Routers)
- 🖨️ **Oficina** (Impresoras)
- 📷 **Fotografía** (Cámaras)

---

## 🎯 **Casos de Uso**

### **1. Pequeñas Empresas**
- Control de inventario básico
- Gestión de productos
- Reportes simples

### **2. Tiendas Online**
- Seguimiento de stock
- Alertas de productos bajos
- Gestión de categorías

### **3. Almacenes**
- Control de entrada/salida
- Auditoría de movimientos
- Reportes de valor

### **4. Emprendedores**
- Demo para clientes
- Prototipo funcional
- Base para desarrollo

---

## 💻 **Arquitectura del Proyecto**

```
sistema-inventario-demo/
├── index.html              # Archivo principal (React CDN)
├── README.md              # Este archivo
└── data/
    └── sample-products.json  # Datos de ejemplo (opcional)
```

### **Estructura del Código**

```javascript
// Componentes Principales
- InventoryManager (Main)
  ├── LoginScreen
  ├── Dashboard
  │   ├── StatsCards
  │   ├── LowStockAlerts
  │   └── CategoryBreakdown
  ├── ProductManagement
  │   ├── SearchBar
  │   ├── Filters
  │   ├── ProductTable
  │   └── CRUD Forms
  └── AuditHistory
```

---

## 🔧 **Personalización**

### **Modificar Usuarios**

```javascript
// En index.html, línea ~XX
const users = [
  { username: 'admin', password: 'admin123', role: 'superadmin', name: 'Administrador' },
  { username: 'viewer', password: 'viewer123', role: 'viewer', name: 'Usuario Consulta' }
];

// Agregar nuevos usuarios o cambiar credenciales
```

### **Cambiar Productos Iniciales**

```javascript
// En index.html, línea ~XX
const sampleProducts = [
  { id: 1, name: 'Tu Producto', category: 'Tu Categoría', ... }
];
```

### **Modificar Colores**

```javascript
// Tailwind CSS classes in HTML
// Ejemplo: bg-blue-600 → bg-purple-600
```

---

## 📈 **Roadmap Futuro**

### **Versión 2.0** (Planeada)
- [ ] Backend con Node.js + Express
- [ ] Base de datos PostgreSQL/MongoDB
- [ ] API RESTful completa
- [ ] Autenticación JWT
- [ ] Multi-tenancy
- [ ] Roles personalizados
- [ ] Reportes PDF
- [ ] Gráficos avanzados (Chart.js)
- [ ] Notificaciones push
- [ ] App móvil (React Native)

### **Mejoras Inmediatas**
- [ ] Validación de formularios mejorada
- [ ] Paginación de productos
- [ ] Búsqueda avanzada
- [ ] Temas personalizables
- [ ] Modo offline (Service Workers)

---

## 🤝 **Contribuciones**

Este es un proyecto de demostración. Si estás interesado en:

- ✨ Contratar desarrollo personalizado
- 🛠️ Soporte técnico
- 📊 Implementación empresarial
- 🎓 Consultoría

**Contáctame:**

📧 Email: alejandro.gutierrezb31@gmail.com  
💼 LinkedIn: [linkedin.com/in/alejandro-gutierrez-9a0318107](https://www.linkedin.com/in/alejandro-gutierrez-9a0318107/)  
💬 WhatsApp: +52 811 048 1221  
🌐 Portfolio: [projectone2020.github.io/portafolio](https://projectone2020.github.io/portafolio/)

---

## 📄 **Licencia**

MIT License - Libre uso para fines educativos y de demostración.

```
Copyright (c) 2024 Alejandro Gutiérrez

Se concede permiso, de forma gratuita, a cualquier persona que obtenga una copia
de este software y archivos de documentación asociados (el "Software"), para utilizar
el Software sin restricciones, incluyendo sin limitación los derechos de usar, copiar,
modificar, fusionar, publicar, distribuir, sublicenciar y/o vender copias del Software.
```

---

## 🌟 **Agradecimientos**

- React Team por el framework
- Tailwind CSS por el sistema de diseño
- Lucide por los iconos
- Netlify por el hosting gratuito

---

## 📞 **Contacto y Soporte**

**Alejandro Gutiérrez**  
*Desarrollador Web Full-Stack*  
*+10 Años de Experiencia*

- 📧 **Email:** alejandro.gutierrezb31@gmail.com
- 💼 **LinkedIn:** [linkedin.com/in/alejandro-gutierrez-9a0318107](https://www.linkedin.com/in/alejandro-gutierrez-9a0318107/)
- 🌐 **Portfolio:** [projectone2020.github.io/portafolio](https://projectone2020.github.io/portafolio/)
- 💬 **WhatsApp:** [+52 811 048 1221](https://wa.me/528110481221)
- 🐙 **GitHub:** [github.com/projectone2020](https://github.com/projectone2020)

---

## ⭐ **Si te gustó este proyecto**

- Dale una ⭐ en GitHub
- Compártelo con colegas
- Sígueme para más proyectos
- Contáctame para trabajar juntos

---

**¿Interesado en una versión personalizada para tu negocio?**  
[💬 Hablemos por WhatsApp](https://wa.me/528110481221?text=Hola%20Alejandro,%20me%20interesa%20el%20Sistema%20de%20Inventario)

---

*Última actualización: Noviembre 2024*
