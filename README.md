# ⚖️ Asistente Normativo CIEMAT

> Consulta la normativa administrativa y legal **sin inventarse nada**.  
> Responde exclusivamente con información de la documentación oficial indexada.

🌐 **[normativa.menarguez-ia.com](https://normativa.menarguez-ia.com)**

---

## ¿Qué es?

Una aplicación web de consulta normativa basada en IA que permite hacer preguntas en lenguaje natural sobre la legislación administrativa española, obteniendo respuestas precisas y citadas directamente de los textos legales oficiales.

**Sin alucinaciones. Sin improvisación. Solo lo que dice la ley.**

---

## 📚 Documentación indexada

| Fuente | Artículos | Descripción |
|--------|-----------|-------------|
| **LCSP — Ley 9/2017** | 290 | Contratos del Sector Público |
| **Ley 39/2015** | 126 | Procedimiento Administrativo Común |
| **Ley 40/2015** | 152 | Régimen Jurídico del Sector Público |
| **EBEP — RDL 5/2015** | 96 | Estatuto Básico del Empleado Público |
| **LGP — Ley 47/2003** | Resumen completo | Ley General Presupuestaria |
| **Tema 6 — Presupuesto** | Resumen completo | Presupuesto del Estado |
| **BOE-A-2026-11873** | 18 fragmentos | OEP CIEMAT 2026 |
| **Instrucción 1/2019** | 7 fragmentos | OIReScon — Contratos Menores |

**Total: 693 fragmentos · 8 fuentes oficiales**

---

## ⚙️ Cómo funciona

```
Pregunta del usuario
        ↓
Búsqueda TF-IDF sobre 693 fragmentos (sin backend)
        ↓
Top 10 fragmentos más relevantes inyectados en el prompt
        ↓
Claude Sonnet responde SOLO con esa información
        ↓
Respuesta citada + fuentes visibles en panel lateral
```

Todo funciona **100% en el navegador** — sin servidor, sin base de datos, sin dependencias externas salvo la API de Anthropic.

---

## 🔑 Requisitos

- API Key de Anthropic (`sk-ant-...`)  
  → Se guarda en `localStorage` del navegador. Nunca sale del dispositivo.

---

## 📋 Casos de uso habituales

- *"¿Cuál es el umbral del contrato menor en CIEMAT?"*
- *"¿Qué requisitos exige el Art. 120 LCSP para tramitar una emergencia?"*
- *"¿Qué documentación necesito para un contrato menor?"*
- *"¿Cuáles son los derechos del empleado público según el EBEP?"*
- *"¿Cuál es el plazo máximo de resolución en procedimiento administrativo?"*

---

## 🏗️ Arquitectura

```
index.html  (694 KB)
├── CSS — Diseño institucional CIEMAT
├── HTML — Interfaz de chat + panel de fragmentos
├── JS — Motor de búsqueda TF-IDF + llamada a API Anthropic
└── DATA — 693 fragmentos embebidos como const CHUNKS = [...]
```

**Single-file app** — desplegada en GitHub Pages con dominio personalizado vía Cloudflare DNS.

---

## 🚀 Despliegue

1. Clona el repo  
2. Abre `index.html` en el navegador  
3. Introduce tu API Key de Anthropic  
4. Empieza a consultar

Para desplegar en tu propio dominio: GitHub Pages + registro CNAME en tu proveedor DNS.

---

## 👤 Autor

**Nacho Menárguez Fernández**  
División de Combustión y Gasificación · CIEMAT  
📧 ignacio.menarguez@ciemat.es

---

## ⚠️ Aviso legal

Esta herramienta es de uso interno y no oficial. Las respuestas se basan en los textos legales oficiales vigentes pero no constituyen asesoramiento jurídico. Ante cualquier duda legal, consulta con el Servicio Jurídico del CIEMAT.

---

*Actualizado: junio 2026 · Documentación vigente a fecha de indexación*
