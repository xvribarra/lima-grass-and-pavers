# Lima Grass & Pavers — High-Conversion Local Business Boilerplate

Landing page bilingüe (EN/ES) de alta conversión diseñada para **Lima Grass & Pavers (Lima Grass LLC)** en Phoenix, AZ, y estructurada como **modelo/boilerplate reutilizable** para negocios locales de servicios en el hogar (*Home & Construction Services*).

---

## 📁 Estructura del Proyecto

```text
.
├── index.html                        # Landing page principal (Tailwind CSS + Schema JSON-LD + Calculadora + i18n EN/ES)
├── assets/
│   └── images/
│       ├── hero-curved-patio.jpg     # Hero & Servicio de Zacate Artificial / Patio Curvo
│       ├── modern-travertine-grid.jpg# Diseño moderno en cuadros de travertino y tiras de zacate
│       ├── scurve-pavers-walkway.jpg # Andador curvo en "S" de adoquín y grava desértica
│       ├── before-after-yard.jpg     # Comparativa Antes y Después de transformación de patio
│       └── travertine-pool-deck.jpg  # Piso de travertino para alberca y patio
└── README.md                         # Guía de Activación de SEO Local y Reutilización del Boilerplate
```

---

## ✅ Guía de Activación de SEO Local (Checklist Automatizable)

### 1. Registro en Google Search Console e Indexación del Schema JSON-LD (`HomeAndConstructionBusiness`)

- [ ] **Paso 1.1 — Alta de Propiedad:**
  1. Ingresa a [Google Search Console](https://search.google.com/search-console).
  2. Selecciona **Añadir propiedad**:
     - Usa **Dominio** (vía registro TXT en DNS) si ya conectaste el dominio personalizado, o **Prefijo de la URL** con la URL HTTPS de producción.
- [ ] **Paso 1.2 — Verificación de Propiedad:**
  1. Si usas **Prefijo de URL**, descarga la etiqueta meta HTML (`<meta name="google-site-verification" content="..." />`) y colócala dentro del `<head>` de `index.html`, o verifica mediante DNS TXT en tu proveedor de dominio / Vercel.
- [ ] **Paso 1.3 — Validación del Schema JSON-LD (`HomeAndConstructionBusiness`):**
  1. Abre la [Prueba de resultados enriquecidos de Google (Rich Results Test)](https://search.google.com/test/rich-results) y el [Validador de Schema.org](https://validator.schema.org/).
  2. Introduce la URL de producción y verifica que el bloque `<script type="application/ld+json">` de tipo `HomeAndConstructionBusiness` sea detectado sin errores ni advertencias críticas:
     - `name`: `"Lima Grass & Pavers"` (`legalName`: `"Lima Grass LLC"`)
     - `telephone`: `"+1-602-472-8846"`
     - `address`: `4128 N 27th Ave, Phoenix, AZ 85017`
     - `geo`: `33.4958, -112.1168`
     - `areaServed`: `Phoenix, Glendale, Peoria, Scottsdale, Tempe, Mesa, Avondale, Chandler`
     - `hasOfferCatalog`: Paver Installation, Artificial Grass & Turf, Travertine Pool Decks & Patios, Decorative Gravel & Desert Landscaping.
- [ ] **Paso 1.4 — Solicitar Indexación Inmediata:**
  1. En Google Search Console, pega la URL principal en la barra superior **Inspección de URLs** (*URL Inspection*).
  2. Haz clic en **Solicitar indexación** (*Request Indexing*) para forzar el rastreo del HTML y del marcado estructurado `HomeAndConstructionBusiness`.

---

### 2. Configuración de Google Business Profile (GBP — Phoenix, AZ)

- [ ] **Paso 2.1 — Creación o Reclamación del Perfil:**
  1. Entra a [Google Business Profile](https://www.google.com/business/).
  2. Registra el nombre comercial exacto: **Lima Grass & Pavers** (manteniendo consistencia NAP — *Name, Address, Phone* — con el Schema JSON-LD del sitio).
- [ ] **Paso 2.2 — Selección de Categorías Comerciales:**
  - **Categoría principal:** `Landscaper` (*Paisajista*)
  - **Categoría secundaria / adicional:** `Paving Contractor` (*Contratista de pavimentación*)
  - *(Opcionales recomendadas)*: `Landscape Designer`, `Masonry Contractor`.
- [ ] **Paso 2.3 — Configuración como *Service-Area Business* (Negocio de Área de Servicio):**
  1. En **Ubicación y áreas**, configura el negocio como **Service-area business** (visitas e instalaciones en el domicilio del cliente).
  2. Si no se reciben clientes sin cita en la oficina base (`4128 N 27th Ave, Phoenix, AZ 85017`), desactiva *"Mostrar dirección comercial a los clientes"* y define explícitamente las ciudades de cobertura:
     - **Phoenix, AZ** (Principal)
     - **Glendale, AZ**
     - **Peoria, AZ**
     - **Scottsdale, AZ**
     - **Tempe, AZ**
     - **Mesa, AZ**
     - **Avondale, AZ**
     - **Chandler, AZ**
- [ ] **Paso 2.4 — Datos Operativos y Activos Visuales:**
  - **Teléfono principal:** `(602) 472-8846`
  - **Sitio web:** URL HTTPS de producción con parámetros UTM opcionales (`?utm_source=gbp&utm_medium=organic`).
  - **Horario de atención:** Lunes a Sábado de `7:00 AM – 5:00 PM` (Domingo cerrado).
  - **Atributos destacados:** *Se habla español / Bilingual service*, *Free estimates / Estimados gratis*, *On-site services*.
  - **Fotografías iniciales:** Sube las 5 imágenes de `assets/images/` en la sección de Fotos del perfil de Google Business.

---

### 3. Configuración de Llamadas, WhatsApp y SMS Directo para `(602) 472-8846`

- [ ] **Paso 3.1 — Botones de Llamada Directa (`tel:`):**
  - Todos los botones de llamada en el encabezado, Hero, sección de contacto y barra flotante móvil utilizan el protocolo estándar:
    ```html
    <a href="tel:6024728846">📞 (602) 472-8846</a>
    ```
  - Verifica en iOS y Android que al tocar el botón se abra el marcador telefónico con `(602) 472-8846`.
- [ ] **Paso 3.2 — Envío de Cotizaciones por WhatsApp (`wa.me`):**
  - El formulario interactivo (`handleLeadSubmit` en `index.html`) construye automáticamente el mensaje prellenado con nombre, teléfono, código postal, servicio y área estimada, redirigiendo a:
    ```text
    https://wa.me/16024728846?text=Hello%20Lima%20Grass%20%26%20Pavers!...
    ```
  - **Requisito en el teléfono del negocio:** Asegúrate de tener instalado **WhatsApp Business** activo con el número `+1 (602) 472-8846`, mensaje de bienvenida automático en inglés/español y catálogo básico de servicios.
- [ ] **Paso 3.3 — Enlace Directo a SMS Nativo (`sms:`) (Alternativa o Botón Secundario):**
  - Para clientes en EE. UU. que prefieran mensaje de texto SMS nativo en lugar de WhatsApp, puedes usar el esquema `sms:` compatible con iOS y Android:
    ```html
    <a href="sms:+16024728846?&body=Hi%20Lima%20Grass%20%26%20Pavers,%20I%20would%20like%20a%20free%20estimate.">
      💬 Text Us: (602) 472-8846
    </a>
    ```
  - **En Google Business Profile:** Activa la opción de **Mensajes / Chat por SMS o WhatsApp** dentro del panel de Google Business Profile vinculando el número `(602) 472-8846` o la URL `https://wa.me/16024728846`.

---

## 🔁 Cómo Reutilizar este Repositorio para Futuros Clientes Locales

1. **Clonar el repositorio base:**
   ```bash
   git clone <URL_DEL_REPOSITORIO> nuevo-cliente-local
   cd nuevo-cliente-local
   ```
2. **Actualizar el bloque JSON-LD (`index.html` líneas 35–84):**
   - Reemplazar `name`, `legalName`, `telephone`, `email`, `address`, `geo`, `areaServed` y `hasOfferCatalog`.
3. **Reemplazar los 5 activos visuales en `assets/images/`:**
   - Mantener relaciones de aspecto horizontales (`16:9` o `4:3`) optimizadas en `.jpg` (`< 300 KB` por imagen).
4. **Actualizar diccionario bilingüe (`translations.en` y `translations.es`) y número en `handleLeadSubmit`:**
   - Reemplazar `tel:6024728846` y `https://wa.me/16024728846` por el teléfono del nuevo cliente.
5. **Desplegar en Vercel:**
   ```bash
   vercel --prod
   ```

