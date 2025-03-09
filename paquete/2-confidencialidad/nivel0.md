# NIVEL 0: REPOSITORIO BÁSICO SEGURO
# OPCIÓN SIN COSTO PARA LA COMPETENCIA DE DATOS

## DESCRIPCIÓN GENERAL

El Nivel 0 proporciona una opción sin costo para equipos con recursos limitados o para proyectos que involucran datos de menor sensibilidad. Esta alternativa mantiene un nivel básico pero efectivo de seguridad utilizando herramientas gratuitas y prácticas de seguridad estándar.

## CASOS DE USO APROPIADOS

Este nivel es adecuado para:
- Datos ya anonimizados o agregados
- Datos sintéticos o parcialmente sintéticos
- Conjuntos de datos de investigación con baja sensibilidad
- Datos sin información personal identificable (IPI)
- Proyectos piloto o educativos

**No se recomienda para:**
- Datos médicos con identificadores personales
- Información financiera individual
- Datos sensibles de menores
- Información comercial altamente confidencial
- Datos sujetos a regulaciones estrictas (HIPAA, GDPR nivel alto, etc.)

## IMPLEMENTACIÓN TÉCNICA

### Componentes Principales

1. **Repositorio Base:** GitHub (plan gratuito) con repositorio privado
   - Cada equipo obtiene almacenamiento gratuito con control de versiones
   - Compatible con control de versiones y gestión de acceso básica

2. **Cifrado de Datos:** VeraCrypt (software gratuito)
   - Creación de contenedores cifrados para almacenar datos sensibles
   - Cifrado AES-256 estándar de la industria

3. **Comunicación Segura:** Signal (gratuito)
   - Grupo privado para intercambio de contraseñas y discusiones sensibles
   - Cifrado de extremo a extremo
   - Mensajes con autodestrucción para información crítica

4. **Autenticación:** Yubikey FIDO U2F (opción asequible ~$25-50 por equipo)
   - Opcional pero altamente recomendado para protección contra phishing
   - Compatible con GitHub y la mayoría de servicios recomendados

## PROTOCOLOS Y PROCEDIMIENTOS

### Configuración Inicial

1. **Preparación de Datos:**
   - El proveedor del problema realiza primera anonimización/agregación básica
   - Se documentan las transformaciones realizadas para transparencia

2. **Establecimiento del Repositorio:**
   - Crear repositorio privado en GitHub
   - Configurar ramas protegidas para prevenir modificaciones accidentales
   - Requerir revisiones de código para cambios

3. **Gestión de Acceso:**
   - Activar autenticación de dos factores para todos los miembros
   - Limitar el acceso solo a colaboradores esenciales
   - Documentar claramente roles y permisos de cada miembro

### Manejo Diario de Datos

1. **Almacenamiento de Datos Sensibles:**
   - Datos almacenados en contenedores VeraCrypt (nunca en texto plano)
   - Archivos cifrados subidos a GitHub como binarios
   - Contraseñas de contenedores compartidas por canal separado (Signal)

2. **Trabajo con los Datos:**
   - Descargar contenedor cifrado localmente
   - Desbloquear en sistema local utilizando contraseña compartida
   - Trabajar con datos solo en memoria/volumen cifrado temporal
   - Nunca almacenar datos descifrados permanentemente
   - Bloquear contenedor cuando no esté en uso activo

3. **Procesamiento y Análisis:**
   - Código de análisis almacenado en GitHub (sin datos sensibles incrustados)
   - Utilizar variables de entorno o archivos de configuración separados para credenciales
   - Implementar prácticas de "clean room" (separación de datos y código)

4. **Compartición de Resultados:**
   - Revisar resultados/outputs antes de compartir para prevenir filtraciones
   - Utilizar estadísticas agregadas cuando sea posible
   - Documentar métodos de anonimización y preservación de privacidad

## PRÁCTICAS DE SEGURIDAD REFORZADAS

Para compensar limitaciones presupuestarias con mayor disciplina:

1. **Rotación Regular de Contraseñas:**
   - Cambiar contraseñas de acceso cada 30 días
   - Utilizar gestor de contraseñas gratuito (como Bitwarden)

2. **Higiene Digital:**
   - Mantener sistemas operativos y software actualizados
   - Utilizar antivirus/antimalware (soluciones gratuitas como Windows Defender)
   - Navegar mediante VPN cuando se acceda al repositorio (ProtonVPN gratuito)

3. **Capacitación Básica:**
   - Completar curso gratuito online sobre seguridad de datos
   - Revisar guías de mejores prácticas proporcionadas por Bayes Plurinacional
   - Realizar pruebas de verificación de conocimientos

4. **Auditoría Manual:**
   - Registro manual de acciones realizadas sobre datos sensibles
   - Revisiones periódicas (semanales) de registro de actividad en GitHub
   - Reporte mensual de actividades al proveedor del problema

## LIMITACIONES CONOCIDAS

Es importante que todos los participantes comprendan las limitaciones de este nivel:

1. **Sin monitoreo automatizado de amenazas**
   - Se depende de vigilancia manual y buenas prácticas

2. **Auditoría limitada**
   - Sin registro detallado de todas las interacciones con los datos

3. **Sin protección contra amenazas avanzadas**
   - Vulnerable a atacantes sofisticados o con recursos significativos

4. **Dependencia del factor humano**
   - Mayor responsabilidad individual para mantener la seguridad

## ACUERDO DE RESPONSABILIDAD

Todos los participantes que utilicen el Nivel 0 deben firmar un acuerdo adicional reconociendo:

1. Comprensión de las limitaciones de seguridad
2. Compromiso con las prácticas de seguridad descritas
3. Responsabilidad compartida por la protección de los datos
4. Aplicabilidad completa del NDA estándar

## PROCESO DE APROBACIÓN

No todos los proyectos serán elegibles para utilizar el Nivel 0:

1. El proveedor del problema debe evaluar y aprobar explícitamente el uso de esta opción
2. El comité de ética de datos de Bayes Plurinacional debe revisar y aprobar la solicitud
3. Se requiere documentación de las medidas de anonimización implementadas
4. Puede requerirse una evaluación de riesgo simplificada

## RECOMENDACIONES PARA MEJORA INCREMENTAL

Para equipos que inicien con Nivel 0 pero deseen mejorar gradualmente:

1. **Mejoras de bajo costo:**
   - Migrar a GitLab gratuito (ofrece CI/CD y más funcionalidades de seguridad)
   - Implementar archivo .gitattributes con git-crypt (cifrado selectivo gratuito)
   - Utilizar herramientas adicionales de análisis de seguridad gratuitas (OWASP ZAP)

2. **Cuando sea posible financieramente:**
   - Actualizar a GitHub Team ($4/usuario/mes) para obtener más seguridad
   - Adquirir almacenamiento cifrado dedicado
   - Implementar una solución VPN pagada más robusta

---

Esta opción Nivel 0 demuestra que la seguridad de los datos no necesariamente requiere grandes inversiones financieras, sino principalmente compromiso con buenas prácticas, educación apropiada y disciplina en su implementación.
