# Introducción a Pyomo

## ¿Qué es Pyomo?

Pyomo (Python Optimization Modeling Objects) es una biblioteca de código abierto en Python que se utiliza para definir y resolver problemas complejos de optimización matemática. Permite modelar problemas de:
- Programación lineal (LP)
- Programación no lineal (NLP)
- Programación entera mixta (MIP/MILP)
- Programación disyuntiva generalizada (GDP)

## Contenido del Repositorio

```
/intro-pyomo
├── python_basico.ipynb            # Notebook introductoria a Python
├── fundamentos_pyomo.ipynb        # Notebook introductoria a Pyomo 
├── optimizacion_discreta.ipynb    # Notebook sobre optimización discreat
├── presentacion_taller_pyomo.pdf  # Diapositivas utilizadas durante el taller
├── LICENSE                        # Licencia
├── pyproject.toml                 # Configuración del environment de Python
└── README.md
```
## Instrucciones de Uso

### Desde GoogleColab
Haz click en cada link para dirigirte al notebook correspondiente:
* Python básico
<a target="_blank" href="https://colab.research.google.com/github/isfons/intro-pyomo/blob/main/python_basico.ipynb">
  <img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"/>
</a>

* Fundamentos Pyomo
<a target="_blank" href="https://colab.research.google.com/github/isfons/intro-pyomo/blob/main/fundamentos_pyomo.ipynb">
  <img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"/>
</a>

* Optimización discreta
<a target="_blank" href="https://colab.research.google.com/github/isfons/intro-pyomo/blob/main/optimizacion_discreta.ipynb">
  <img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"/>
</a>

### Uso local

1. Clona este repositorio:
   ```bash
   git clone https://github.com/isfons/intro-pyomo.git
   cd intro_pyomo
   ```

2. Asegúrate de tener instalados todos los [requisitos](#requisitos-previos) mencionados abajo.

3. Abre cada uno de los notebook (`*.ipynb`)


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

## Recursos Adicionales

- [Documentación oficial de Pyomo](https://pyomo.readthedocs.io/)
- [Lista de solvers soportados](https://pyomo.readthedocs.io/en/stable/getting_started/solvers.html)
- [Instalación de Pyomo](https://pyomo.readthedocs.io/en/stable/getting_started/installation.html)

## Licencia

Ver el archivo [LICENSE](LICENSE) para más detalles.