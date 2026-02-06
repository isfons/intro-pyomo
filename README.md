# Introducción a Pyomo

## ¿Qué es Pyomo?

Pyomo (Python Optimization Modeling Objects) es una biblioteca de código abierto en Python que se utiliza para definir y resolver problemas complejos de optimización matemática. Permite modelar problemas de:
- Programación lineal (LP)
- Programación no lineal (NLP)
- Programación entera mixta (MIP/MILP)
- Programación disyuntiva generalizada (GDP)

## Contenido del Repositorio

Este repositorio incluye los siguientes notebooks:

### 0. `python_basico.ipynb` 
Fundamentos de básicos de Python requeridos para iniciarse en Pyomo:
- **Sintaxis básica**: variables, operaciones, indexación (¡empieza en 0!)
- **Estructuras de datos**: listas, tuplas y diccionarios (esenciales para Pyomo)
- **Bucles y comprensiones**: iteración y generación de expresiones compactas
- **Funciones**: definición de funciones y funciones lambda

### 1. `fundamentos_pyomo.ipynb`
Introducción a los conceptos básicos de Pyomo:
- **Instalación y configuración** de Pyomo y solvers (IPOPT, GLPK)
- **Ejemplo 1: Problema teórico (NLP)** - Optimización no lineal con restricciones de igualdad
- **Ejemplo 2: Problema de mezcla lineal** - Aplicación práctica en la industria cervecera

**Conceptos cubiertos:**
- Modelos concretos vs abstractos
- Declaración de variables, parámetros y restricciones
- Definición de funciones objetivo
- Uso de sets e indexación
- Resolución con diferentes solvers
- Inspección y visualización de resultados

### 2. `optimizacion_discreta.ipynb`
Optimización con variables discretas y restricciones lógicas:
- **Ejemplo 1: Problema de ubicación de almacenes** - Variables binarias y optimización de redes de distribución
- **Ejemplo 2: Formulación de mezclas con incompatibilidades** - Restricciones lógicas y disyunciones

**Conceptos cubiertos:**
- Modelos abstractos y carga de datos
- Variables binarias y enteras
- Restricciones lógicas
- Reformulación Big-M
- Envolvente convexa (convex hull)
- Programación disyuntiva generalizada (GDP)
- Análisis de sensibilidad

## Requisitos Previos

Para utilizar estos notebooks necesitas:

### 1. Python ≥ 3.8

Asegúrate de tener Python instalado. Verifica tu versión con:
```bash
python --version
```

### 2. Dependencias de Python

Instala las dependencias del proyecto usando pip:
```bash
pip install -e .
```

O manualmente:
```bash
pip install pyomo numpy pandas matplotlib ipykernel
```

### 3. **Solvers de Optimización (REQUERIDO)**

⚠️ **IMPORTANTE**: Pyomo es solo un lenguaje de modelado. Para resolver problemas de optimización, **debes instalar los solvers externos obligatoriamente**.

#### **IPOPT** (para problemas no lineales - NLP)

**Instalación recomendada con Conda:**
```bash
conda install -c conda-forge ipopt
```

**Alternativa - Descarga manual:**
- Windows: [Descargar binarios](https://github.com/coin-or/Ipopt/releases)
- Linux/Mac: Compilar desde el código fuente o usar gestores de paquetes del sistema

**Verificar instalación:**
```bash
pyomo help --solvers
```
Deberías ver `ipopt` en la lista de solvers disponibles.

#### **GLPK** (para problemas lineales y enteros - LP/MILP)

**Instalación recomendada con Conda:**
```bash
conda install -c conda-forge glpk
```

**Alternativa en Linux:**
```bash
sudo apt-get install glpk-utils 
```

**Alternativa en Windows:**
Descargar desde [GNU GLPK](https://www.gnu.org/software/glpk/) y añadir al PATH del sistema.

**Verificar instalación:**
```bash
glpsol --version
```

#### Instalación rápida de ambos solvers (Conda):
```bash
conda install -c conda-forge ipopt glpk
```

## Instrucciones de Uso

1. Clona este repositorio:
   ```bash
   git clone https://github.com/tu-usuario/intro_pyomo.git
   cd intro_pyomo
   ```

2. Asegúrate de tener instalados todos los requisitos mencionados arriba.

3. Abre los notebooks en orden:
   - **Si tienes poca experiencia con Python**: Empieza con `python_basico.ipynb` para aprender los fundamentos necesarios
   - Continúa con `fundamentos_pyomo.ipynb` para entender los conceptos básicos de optimización
   - Avanza a `optimizacion_discreta.ipynb` para problemas más avanzados con variables discretas
   
4. Los notebooks están diseñados como **plantillas para estudiantes**. Completa los ejercicios y tareas indicadas en cada sección.

## Recursos Adicionales

- [Documentación oficial de Pyomo](https://pyomo.readthedocs.io/)
- [Lista de solvers soportados](https://pyomo.readthedocs.io/en/stable/getting_started/solvers.html)
- [Instalación de Pyomo](https://pyomo.readthedocs.io/en/stable/getting_started/installation.html)

## Licencia

Ver el archivo [LICENSE](LICENSE) para más detalles.