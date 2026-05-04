# Criterios de Aceptación - Sprint 1

**Formato:** Given-When-Then  
**Redactado por:** Lorena López Bermúdez (Scrum Master)  
**Fecha:** 4 mayo 2026  
**Sprint:** Sprint 1 (24-29 abril 2026)

---

## US-01: Crear empresa (ALB-1) - 5 SP

### Criterio 1 — Alta exitosa de empresa
GIVEN el visitante accede al formulario de registro y no existe ninguna empresa con CIF "B87654321" ni usuario con email "juan.lopez@transportesportes.es.", sector "Logísitca", contraseña "Pass1234!" y hace clic en "Crear Cuenta"
WHEN el visitante completa el formulario con nombre "Transportes Portes", CIF "B87654321", email admin "juan.lopez@transportesportes.es", sector "logística", contraseña "Pass1234!" y hace clic en "Crear Cuenta"
THEN se crea la empresa en la tabla `empresas` con `empresa_id` único generado, `nombre`="Trasnportes Portes", `cif`="B87654321", `email_admin`="juan.lopez@transportesporte.es", `sector`="Logística", se crea el usuario admin en la tabla `usuarios` con `usuario_id`único, `empresa_id`apuntando a la empresa creada, `email`="juan.perez@trasportesportes.es", `nombre`="Juan López", `rol`= "admin", contraseña hasheada, se genera un token JWT que contiene `user_id`, `empresa_id`y `rol`="admin", se guarda en local storage y se redirige a /panel

### Criterio 2 — Alta exitosa de empresa
