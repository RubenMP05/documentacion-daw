### 📄 `docs/pruebas/analisis_caja_blanca.md`
```markdown
# Análisis de Caja Blanca

Para asegurar la calidad de la lógica interna de TaskFlow, aplicamos técnicas de pruebas de caja blanca sobre los métodos críticos del sistema.

## Método evaluado: `cambiarEstado(nuevoEstado)` de la clase Tarea

**Código fuente simplificado:**
```javascript
function cambiarEstado(tarea, nuevoEstado) {
  if (!tarea) throw new Error("Tarea nula");
  if (tarea.estado === 'Completada' && nuevoEstado === 'Pendiente') {
      throw new Error("Transición inválida");
  }
  tarea.estado = nuevoEstado;
  return tarea;
}
