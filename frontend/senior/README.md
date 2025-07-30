# TaxDown Frontend Challenge

## Sobre la posición 💻
Como Frontend Engineer, buscamos a alguien que sepa aplicar las mejores soluciones a los problemas que pueden aparecer en una aplicación web moderna. Esta prueba evaluará tu capacidad para diseñar arquitecturas escalables y mantener código de calidad profesional.

## Lo que buscamos evaluar
- **Arquitectura de componentes**: Diseño escalable y reutilizable
- **Principios SOLID**: Aplicación práctica en frontend  
- **Abstracción**: Separación de responsabilidades y dependencias
- **Gestión de estado**: Solución apropiada para el problema
- **Gestión de rutas**: Navegación fluida y consistente
- **Testing**: Cobertura y calidad de las pruebas
- **Criterio técnico**: Justificación de decisiones arquitecturales

## El Problema 🎯

Necesitas construir una **aplicación de gestión de declaraciones fiscales** que permita:

### 1. Autenticación de Usuario
- Implementa un sistema de login (puede ser simulado)
- Una vez autenticado, el usuario accede al dashboard principal

### 2. Dashboard de Declaraciones
- Muestra una lista de declaraciones fiscales del usuario
- Cada declaración tiene información básica (año, nombre, estado, etc.)
- Permite acceder a cada declaración para gestionar submissions

### 3. Sistema de Formularios Dinámicos
**Este es el core del challenge:**
- Cada declaración tiene un formulario asociado con campos dinámicos
- Los campos pueden variar en tipo, validaciones y configuración
- El formulario debe renderizarse dinámicamente basado en una configuración
- Debe manejar diferentes tipos de input (text, number, select, etc.)
- Debe implementar validaciones configurables

### 4. Gestión de Submissions
- Permite crear nuevas submissions completando el formulario
- Almacena y lista las submissions realizadas para cada declaración
- Permite filtrar/buscar submissions por diferentes criterios
- **Bonus**: Edición y eliminación de submissions

## Requisitos Técnicos

### Obligatorios
- **React** como biblioteca base
- **Testing** con cobertura mínima del 60%
- **TypeScript** preferiblemente
- Código limpio y documentado

### Libertad Total
- **Gestión de estado**: Context, Redux, Zustand, Jotai, etc.
- **Routing**: React Router, Next.js, Reach Router, etc.
- **Styling**: CSS modules, Styled Components, Tailwind, etc.
- **Forms**: React Hook Form, Formik, custom solution, etc.
- **Data fetching**: Fetch, Axios, SWR, React Query, etc.
- **Build tool**: Vite, Next.js, CRA, Webpack, etc.

## Datos de Ejemplo

Puedes usar datos mockeados, localStorage, o implementar una API simple. Como referencia:

```json
// Declaraciones
{
  "taxes": [
    {
      "id": "1",
      "name": "Declaración 2023",
      "year": "2023",
      "status": "active"
    }
  ]
}

// Configuración de formulario dinámico
{
  "formConfig": [
    {
      "id": "name",
      "type": "text",
      "label": "Nombre",
      "required": true,
      "maxLength": 20
    },
    {
      "id": "income",
      "type": "number",
      "label": "Ingresos anuales",
      "required": true,
      "min": 0
    }
  ]
}
```

## Entregables 📦

1. **Código fuente** en repositorio privado
2. **README** con:
   - Instrucciones de instalación y ejecución
   - Decisiones arquitecturales y justificación
   - Tecnologías elegidas y por qué
   - Próximos pasos o mejoras identificadas
3. **Tests** ejecutables
4. **Aplicación desplegada** (opcional pero valorado)

## Evaluación 📊

### Criterios principales:
- **Arquitectura**: ¿Es escalable y mantenible?
- **Calidad de código**: ¿Es legible y sigue buenas prácticas?
- **Flexibilidad**: ¿El sistema de formularios es realmente dinámico?
- **Testing**: ¿Las pruebas aportan confianza al sistema?
- **Criterio**: ¿Las decisiones técnicas están bien fundamentadas?

### En la defensa oral evaluaremos:
- Justificación de decisiones arquitecturales
- Capacidad de extensión del sistema
- Identificación de trade-offs
- Propuestas de mejora y escalabilidad

## Filosofía de la Prueba 🎭

- **Usa IA**: Está permitido y es bienvenido el uso de herramientas de IA
- **Piensa en producción**: Como si fuera código real que va a evolucionar
- **Demuestra madurez**: Esperamos código de nivel senior
- **Sé pragmático**: No over-engineering, pero tampoco shortcuts que comprometan calidad

## Entrega
Comparte tu repositorio privado con [Fernán Ramos](https://github.com/Fernan-Ramos) para la revisión.

---

**¡Disfruta el reto y demuestra tu mejor nivel!** 🚀

*Tiempo estimado: 4-8 horas (ajusta según tu disponibilidad)* 
