# Análisis Previo - US-014: Ranking Semántico

> Análisis detallado de recursos, distribución de trabajo y dependencias para la User Story US-014  
> Fecha: Julio 2025  
> Product Manager: [Nombre]  
> Tech Lead: [Nombre]

---

## 📋 Resumen Ejecutivo

**US-014: Ranking Semántico** es la **funcionalidad diferenciadora clave** del producto que requiere **3 sprints (6 semanas)** para implementación completa. Requiere equipo especializado en AI/ML y arquitectura vectorial escalable. La distribución está dominada por Backend/AI (80%) con componente Frontend sofisticado para explicabilidad.

---

## 📊 Desglose de Tickets y Estimaciones

| **Ticket** | **Descripción** | **Equipo** | **SP** | **Días** | **Complejidad** |
|------------|-----------------|------------|--------|----------|-----------------|
| **T001_formulario** | Infraestructura de embeddings y vectores | AI/ML + Backend | 8 SP | 8-10 días | **Muy Alta** |
| **T002_validacion** | Algoritmo validación y calibración scores | AI/ML | 5 SP | 5-7 días | **Alta** |
| **T003_guardado** | Sistema persistencia scores y rankings | Backend | 4 SP | 4-5 días | Media |
| **T004_interfaz** | Interfaz ranking y explicabilidad | Frontend | 4 SP | 4-5 días | **Alta** |
| **TOTAL** | | | **21 SP** | **21-27 días** | |

---

## 👥 Recursos Necesarios para 3 Sprints

### **🎯 Configuración Mínima:**
- **1 Senior ML Engineer** - 100% dedicación (especialista embeddings/NLP)
- **1 Senior Backend Developer** - 80% dedicación (arquitectura vectorial)
- **1 Senior Frontend Developer** - 60% dedicación (UI explicabilidad)
- **0.5 Data Scientist** - calibración y métricas
- **0.5 DevOps Engineer** - infraestructura ML/vectorial
- **0.3 Product Owner** - validación criterios de negocio

### **🚀 Configuración Óptima:**
- **1 Senior ML Engineer** + **1 ML Engineer** (para A/B testing)
- **1 Senior Backend Developer** + **1 Backend Developer** (APIs + DB)
- **1 Senior Frontend Developer** + **0.5 UX Designer** (explicabilidad)
- **0.5 Data Scientist** - experimentos y métricas
- **0.5 DevOps Engineer** - scaling y monitoring
- **0.3 Product Owner**
- **0.2 QA Engineer** - testing algorithmic bias

---

## 📈 Distribución de Trabajo por Equipos

### **Por Story Points:**
| **Equipo** | **Story Points** | **Porcentaje** | **Responsabilidades** |
|------------|------------------|----------------|-----------------------|
| **AI/ML** | 13 SP (T001+T002) | **62%** | Embeddings, algoritmos, calibración |
| **Backend** | 4 SP (T003) | **19%** | Persistencia vectorial, APIs performance |
| **Frontend** | 4 SP (T004) | **19%** | UI explicabilidad, visualización scores |

### **Por Complejidad Técnica:**
| **Equipo** | **Muy Alta** | **Alta** | **Media** | **Baja** |
|------------|--------------|----------|-----------|----------|
| **AI/ML** | 60% (T001) | 40% (T002) | 0% | 0% |
| **Backend** | 0% | 0% | 100% (T003) | 0% |
| **Frontend** | 0% | 100% (T004) | 0% | 0% |

### **Por Tiempo Real:**
- **AI/ML**: 13-17 días de trabajo efectivo
- **Backend**: 4-5 días de trabajo efectivo (alta especialización)
- **Frontend**: 4-5 días de trabajo efectivo (UX compleja)
- **Investigación/Experimentos**: 5-7 días adicionales

---

## 🔗 Análisis de Dependencias

### **Dependencias Críticas:**
```
Research ML Models → T001 (Embeddings) → T002 (Algoritmo) → T003 (Persistencia) → T004 (Interfaz)
                                      ↓
                              T003 (Database Vectorial) ← Arquitectura Performance
```

### **Dependencias Externas Críticas:**
- 🔴 **Servicios ML** - OpenAI API, HuggingFace, Sentence-BERT
- 🔴 **Base de datos vectorial** - Pinecone, Weaviate, o Elasticsearch con vectores
- 🔴 **US-008 completada** - datos de CVs parseados para embeddings
- 🔴 **Infraestructura GPU** - para modelos locales (alternativa a APIs)
- ✅ **Cache system** - Redis para scores frecuentes
- ✅ **Monitoring ML** - métricas de modelo y drift detection

### **Secuencia Óptima de Desarrollo:**

#### **🟦 Sprint 1 (Semanas 1-2): Research & Infrastructure**
**Días 1-4: Investigación ML**
- 🔍 **Spike**: Evaluación modelos embeddings (OpenAI vs. Sentence-BERT vs. multilingual)
- 🔍 **Spike**: Testing accuracy con CVs+vacantes reales
- 🔍 **Spike**: Performance y costos por embedding

**Días 5-10: Infrastructure Setup**
- ✅ **T001: Embeddings** - INICIO (setup pipeline, APIs)
- ✅ **Vector DB setup** - configuración Pinecone/Elasticsearch
- ✅ **Monitoring setup** - métricas ML y performance

#### **🟦 Sprint 2 (Semanas 3-4): Core Algorithm**
**Días 11-15: Embeddings Pipeline**
- ✅ **T001: Embeddings** - COMPLETAR (generación, storage, cache)
- ✅ **T002: Algoritmo** - DESARROLLO (similarity, ranking)
- ✅ **T003: Persistencia** - INICIO (schema scores)

**Días 16-20: Algorithm Tuning**
- ✅ **T002: Algoritmo** - CALIBRACIÓN con datos reales
- ✅ **T003: Persistencia** - DESARROLLO (APIs, cache)
- ✅ **Integration testing** - pipeline completo

#### **🟦 Sprint 3 (Semanas 5-6): UI & Production**
**Días 21-25: Interface Development**
- ✅ **T002: Algoritmo** - FINALIZAR (A/B testing setup)
- ✅ **T003: Persistencia** - COMPLETAR (optimization)
- ✅ **T004: Interfaz** - DESARROLLO (ranking UI, explicabilidad)

**Días 26-30: Production Ready**
- ✅ **T004: Interfaz** - COMPLETAR (UX testing)
- ✅ **Performance optimization** - latencia <500ms
- ✅ **Production deployment** - monitoring, alertas

---

## ⚠️ Gestión de Riesgos (CRÍTICA)

### **Riesgos de Impacto Crítico:**

| **Riesgo** | **Probabilidad** | **Impacto** | **Mitigación** |
|------------|------------------|-------------|----------------|
| **Accuracy modelo <70%** | Media | **Crítico** | Spike extensivo día 1-4, múltiples modelos |
| **Latencia >2 segundos** | Alta | **Crítico** | Arquitectura cache + precompute rankings |
| **Costos ML API excesivos** | Alta | Alto | Budget cap + modelos locales como backup |
| **Bias algorítmico** | Media | **Crítico** | Testing diversidad, auditoría AI ethics |
| **Explicabilidad insuficiente** | Media | Alto | UX research, A/B testing interfaces |
| **Escalabilidad vectorial** | Media | Alto | Sharding estrategia, DB vectorial escalable |

### **Riesgos Técnicos Específicos:**
- **Embeddings multi-idioma**: Accuracy puede variar por idioma
- **Cold start**: Nuevas vacantes sin histórico de matches
- **Data drift**: Modelos pueden degradarse con el tiempo
- **Vector dimensionality**: Balance accuracy vs. storage/performance

---

## 🔬 Investigación Técnica Crítica

### **Spike 1: Model Selection (3-4 días)**
**Modelos a evaluar:**
- **OpenAI text-embedding-ada-002**: $0.0001 per 1K tokens, 1536 dim, multilingual
- **Sentence-BERT multilingual**: Free, self-hosted, 768 dim
- **BGE-M3**: Nuevo SOTA, multilingual, free pero requiere GPU
- **Cohere Embed**: $0.0001 per 1K tokens, buena calidad

**Criterios de evaluación:**
- **Accuracy**: Correlation con manual rankings (target >0.8)
- **Multilingüe**: Performance en ES, EN, FR, DE, IT
- **Performance**: Latencia embedding generation (<1 seg)
- **Costo**: Budget sustainable para scaling
- **Maintenance**: Self-hosted vs. API reliability

### **Spike 2: Algorithm Design (2-3 días)**
**Enfoques a evaluar:**
- **Cosine similarity simple**: Baseline rápido
- **Weighted scoring**: Skills vs. Experience vs. Location
- **Learning-to-rank**: ML para optimizar ranking
- **Hybrid approach**: Semantic + traditional filters

### **Spike 3: Vector Database (1-2 días)**
**Opciones:**
- **Pinecone**: Managed, $70/month starter, fácil scaling
- **Weaviate**: Open source + cloud, más control
- **Elasticsearch**: Ya familiar, vector support reciente
- **Chroma**: Open source, lightweight, good for POC

---

## 💡 Recomendaciones para Éxito de 3 Sprints

### **🎯 Setup Pre-Sprint 1:**
1. **Dataset real CVs+Vacantes** para testing (200+ pares)
2. **Accounts ML services** configuradas con budgets
3. **Manual rankings** de referencia (gold standard)
4. **Performance benchmarks** definidos
5. **Ethics/Bias guidelines** para AI fairness

### **🚀 Durante Desarrollo:**
1. **Spikes OBLIGATORIOS** primeros 4 días
2. **A/B testing framework** desde Sprint 2
3. **Performance monitoring** cada commit
4. **Bias testing** con datos demográficos
5. **Business validation** weekly con recruiters reales

### **📊 Métricas de Seguimiento:**
- **Accuracy**: Correlation >0.8 con manual rankings
- **Performance**: <500ms query time para 1000 candidatos
- **Relevance**: Top 5 candidates include 80% of manual picks
- **Bias**: No discriminación por género, edad, origen
- **Explainability**: Users understand 80% of score factors

---

## 🏆 Conclusión y Viabilidad

### **🚨 ALTA COMPLEJIDAD - Requiere 3 Sprints con:**
- **Equipo ML especializado**: Experience en embeddings y NLP
- **Investigación extensiva**: 25% tiempo en spikes y experimentos
- **Infraestructura robusta**: Vector DB, cache, monitoring ML
- **Validación continua**: Business value + technical metrics

### **🎯 Factores Críticos de Éxito:**
1. **Model selection correcta** - accuracy vs. cost balance
2. **Algorithm calibration** - business rules + ML optimization
3. **Performance architecture** - sub-second query times
4. **Explainability UX** - users trust and understand rankings
5. **Bias prevention** - fair and ethical AI implementation

### **📈 Criterios de Aceptación:**
- **Funcionalidad**: Ranking semántico end-to-end
- **Accuracy**: >80% correlation con expert rankings
- **Performance**: <500ms ranking 1000 candidatos
- **Explainability**: Score factors clearly visible
- **Fairness**: No bias en protected characteristics

### **🚨 Señales de Alerta:**
- Accuracy <70% después de 2 semanas → Revaluar approach
- Latency >2 segundos → Rediseñar arquitectura
- Costos >$1000/month → Switch a modelos locales
- Users don't trust rankings → UX research needed
- Bias detected → Stop deployment hasta mitigation

### **💰 Consideraciones de Costo:**
- **OpenAI API**: ~$200-500/month para 10K matches/día
- **Vector DB**: ~$100-300/month dependiendo de solución
- **Infrastructure**: ~$200-400/month para GPU instances
- **Total estimate**: $500-1200/month operational costs

---

**Última actualización**: 13/07/2025  
**Próxima revisión**: Pre-Sprint Planning
